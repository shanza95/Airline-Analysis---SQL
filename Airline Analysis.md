
```sql
create database airline_analysis;
use airline_analysis;
```


## Task 1: Display passengers in routes 01–25

```sql
select * from passengers_on_flights
where route_id between 01 and 25;
```


## Task 2: Business class revenue summary

```sql
select sum(no_of_tickets) as no_of_passengers, sum(no_of_tickets*Price_per_ticket) as total_revenue 
from ticket_details
where class_id = 'Business';
```


## Task 3: Customer full names

```sql
select concat(first_name, ' ', last_name) as Full_Name from customer;
```


## Task 4: Registered & booked customers

```sql
	select c.customer_id, c.first_name, c.last_name,
		td.aircraft_id, td.a_code, td.p_date
from 
	customer c
join
	ticket_details td
on c.customer_id = td.customer_id;
```


## Task 5: Emirates customer names
```sql
select c.first_name, c.last_name, c.customer_id, td.brand
from 
	customer c 
join
	ticket_details td 
on 
	c.customer_id = td.customer_id
where
	td.brand = 'Emirates';
```


## Task 6: Economy Plus travellers

```sql
select customer_id, count(*) as total_flights from passengers_on_flights
where class_id ='Economy Plus'
group by customer_id
having count(*)>0;				
```


## Task 7: Revenue greater than 10000 check

```sql
select sum(no_of_tickets*Price_per_ticket) as Revenue,
if(sum(no_of_tickets*Price_per_ticket) > 10000, 'Yes', 'No') as revenue_crossed_10000
from ticket_details;
```


## Task 8: Create & grant user access

```sql
CREATE USER 'new_user' @ 'localhost' IDENTIFIED BY 'user_password';
GRANT ALL PRIVILEGES ON database_name. * TO 'new_user' @ 'localhost';
# In case we want to grant access with Limited Permissions
GRANT SELECT, INSERT, UPDATE ON database_name. * TO 'new_user' @ 'localhost';
```


## Task 9: Max ticket price per class

```sql
select customer_id, class_id, Price_per_ticket, 
MAX(Price_per_ticket) OVER (PARTITION BY customer_id ORDER BY class_id) as max_ticket_price 
from ticket_details; 
```


## Task 10: Passengers with route_id 4

```sql
select * from passengers_on_flights where route_id = 4;

# create index for query speed
CREATE INDEX idx_route_id ON passengers_on_flights(route_id);

# for the route_id 4, WAQ to view the execution plan of the passengers_on_flights table.
	
EXPLAIN select * from passengers_on_flights where route_id = 4; 

# roll up by row type
	
	SELECT 
    customer_id,
    aircraft_id,
    SUM(Price_per_ticket) AS total_price_all_tickets,
    
    CASE
        WHEN GROUPING(customer_id) = 1 AND GROUPING(aircraft_id) = 1 THEN 'Grand Total'
        WHEN GROUPING(aircraft_id) = 1 THEN 'Subtotal'
        ELSE 'Detail'
    END AS row_type
FROM 
    ticket_details
GROUP BY 
    customer_id, aircraft_id WITH ROLLUP;
```


## Task 11: Total tickets price per customer

```sql
select customer_id, aircraft_id, sum(Price_per_ticket) as tot_price_all_tickets
from ticket_details
group by customer_id, aircraft_id 
with rollup ;
```


## Task 12: Business class view

```sql
CREATE  OR REPLACE VIEW business_class_customers AS
SELECT customer_id, class_id, brand
FROM ticket_details
WHERE class_id ='Business';
```


## Task 13: Stored procedure: passengers by route

```sql
DROP procedure IF EXISTS `get_passengers_by_route`;

DELIMITER //

CREATE PROCEDURE get_passengers_by_route(
    IN from_location VARCHAR(50),
    IN to_location VARCHAR(50)
)
BEGIN
DECLARE EXIT HANDLER FOR SQLEXCEPTION
    BEGIN
        SELECT 'Error: passengers_on_flights table does not exist or query failed.' AS error_message;
    END;
    SELECT *
    FROM passengers_on_flights
    WHERE depart = from_location AND arrival = to_location;
END;
//

DELIMITER ;


CALL get_passengers_by_route('CRW', 'COD');
```


## Task 14: Stored procedure: routes more than 2000 miles

```sql
DELIMITER //

CREATE PROCEDURE get_long_distance_routes()
BEGIN
    SELECT *
    FROM route_details
    WHERE distance_miles > 2000;
END;
//

DELIMITER ;

CALL get_long_distance_routes();
```


## Task 15: Categorize flight distance

/* The categories are:
- short distance travel (SDT) for >=0 AND <= 2000 miles, 
- intermediate distance travel (IDT) for >2000 AND <=6500, 
- long-distance travel (LDT) for >6500.
*/

```sql
DROP procedure IF EXISTS `travel_distance`;

DELIMITER $$
USE `airline_analysis`$$
CREATE PROCEDURE travel_distance (IN distance_miles INT)
BEGIN
	IF distance_miles >=0 AND distance_miles <=2000 THEN SELECT 'STD' AS travel_category;
	ELSEIF distance_miles >2000 AND distance_miles <=6500 THEN SELECT 'ITD' AS travel_category;
	ELSEIF distance_miles >6500 THEN SELECT 'LTD' AS travel_category;
	ELSE SELECT 'distance_miles_not_categorized' AS travel_category;
	END IF;
END$$

DELIMITER ;
CALL travel_distance(2500);
```


## Task 16: Complimentary service per class
	
/* Condition:
- if the class is Business and Economy Plus, then complimentary services are given Yes,
- else it's No
*/

```sql

# CREATE THE STORED FUNCTION
DELIMITER //

CREATE FUNCTION get_complimentary_service(class_name VARCHAR(50))
RETURNS VARCHAR(3)
DETERMINISTIC
BEGIN
    IF class_name IN ('Business', 'Economy Plus') THEN
        RETURN 'Yes';
    ELSE
        RETURN 'No';
    END IF;
END;
//

DELIMITER ;

# CREATE THE STORED PROCEDURE
DELIMITER //

CREATE PROCEDURE get_ticket_services()
BEGIN
    SELECT 
        p_date AS purchase_date,
        customer_id,
        class_id,
        get_complimentary_service(class_id) AS complimentary_service
    FROM 
        ticket_details;
END;
//

DELIMITER ;
CALL get_ticket_services();

DELIMITER //
```


## Task 17: First customer with last name Scott

```sql

CREATE PROCEDURE get_first_scott_customer()
BEGIN
    DECLARE done INT DEFAULT FALSE;
    DECLARE cust_id INT;
    DECLARE fname VARCHAR(50);
    DECLARE lname VARCHAR(50);

    DECLARE cur CURSOR FOR
        SELECT customer_id, first_name, last_name
        FROM customer
        WHERE last_name LIKE '%Scott';

    DECLARE CONTINUE HANDLER FOR NOT FOUND SET done = TRUE;

    OPEN cur;
    FETCH cur INTO cust_id, fname, lname;

    IF NOT done THEN
        SELECT cust_id AS customer_id, fname AS first_name, lname AS last_name;
    END IF;

    CLOSE cur;
END;
//

DELIMITER ;
CALL get_first_scott_customer();
```
