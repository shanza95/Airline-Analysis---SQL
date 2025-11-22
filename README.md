# Airline-Analysis---SQL

### Project Overview
This project simulates a real-world database management scenario for an aviation company named Air Cargo, which offers both passenger and freight services through partnerships with other airlines. The objective is to analyze air travel data to improve operational efficiency, optimize route planning, and enhance the customer experience.

### Insights
- Datasets can be found [here](1697127247_airlines_datasets/)
- SQL Queries can be found [here](Airline%20Analysis.md/)
- SQL Query Tables, in csv file format, can be found [here](SQL%20Query%20Results/)
  
### Business Problem
Air Cargo wants to gain deeper insights into its operations by identifying:
- Regular passengers (to offer loyalty benefits)
- Busiest routes (to better allocate aircraft)
- Ticket sales patterns (to improve revenue and pricing strategy).

✈️ MySQL Airline Database – DBA Tasks

This repository contains SQL queries and stored procedures executed on an airline management database.
All CSV query outputs are organized in the /results folder and referenced by query name.

As a DBA you need to perform the following operations:

| Task # | Query Statement | SQL Query | Result CSV |
|--------|----------------|-----------|------------|
| **1** | WAQ to display all the passengers (customers) who have travelled in routes 01 to 25 | [SQL](Airline%20Analysis.md#task-1-waq-to-display-all-the-passengers-customers-who-have-travelled-in-routes-01-to-25) | [route 01-25.csv](SQL%20Query%20Results/route%2001-25.csv) |
| **2** | WAQ to identify the number of passengers and total revenue in business class from the ticket_details table | [SQL](Airline%20Analysis.md#task-2-waq-to-identify-the-number-of-passengers-and-total-revenue-in-business-class-from-the-ticket_details-table) | [total revenue.csv](SQL%20Query%20Results/total%20revenue.csv) |
| **3** | WAQ to display the full name of the customer by extracting the first name and last name from the customer table | [SQL](Airline%20Analysis.md#task-3-waq-to-display-the-full-name-of-the-customer-by-extracting-the-first-name-and-last-name-from-the-customer-table) | [customers full name.csv](SQL%20Query%20Results/customers%20full%20name.csv) |
| **4** | WAQ to extract the customers who have registered and booked a ticket. Use data from customer and ticket_details tables | [SQL](Airline%20Analysis.md#task-4-waq-to-extract-the-customers-who-have-registered-and-booked-a-ticket-use-data-from-customer-and-ticket_details-tables) | [registered customers.csv](SQL%20Query%20Results/registered%20customers.csv) |
| **5** | WAQ to identify the customer's first name and last name based on their customer_id and brand (Emirates) from the ticket_details table | [SQL](Airline%20Analysis.md#task-5-waq-to-identify-the-customers-first-name-and-last-name-based-on-their-customer_id-and-brand-emirates-from-the-ticket_details-table) | [Emirates Customers.csv](SQL%20Query%20Results/Emirates%20Customers.csv) |
| **6** | WAQ to identify the customers who have travelled by Economy Plus class | [SQL](Airline%20Analysis.md#task-6-waq-to-identify-the-customers-who-have-travelled-by-economy-plus-class) | [Economy_Plus Class Passengers.csv](SQL%20Query%20Results/Economy_Plus%20Class%20Passengers.csv) |
| **7** | WAQ to identify whether the revenue has crossed 10000 using the IF CLAUSE on the ticket_details table | [SQL](Airline%20Analysis.md#task-7-waq-to-identify-whether-the-revenue-has-crossed-10000-using-the-if-clause-on-the-ticket_details-table) | [Revenue more than 10000.csv](SQL%20Query%20Results/Revenue%20more%20than%2010000.csv) |
| **8** | WAQ to create and grant access to a new user to perform operations on a database | [SQL](Airline%20Analysis.md#task-8-waq-to-create-and-grant-access-to-a-new-user-to-perform-operations-on-a-database) | *(No CSV – administrative task)* |
| **9** | WAQ to find the maximum ticket price for each class using window functions on the ticket_details table | [SQL](Airline%20Analysis.md#task-9-waq-to-find-the-maximum-ticket-price-for-each-class-using-window-functions-on-the-ticket_details-table) | [max ticket_price.csv](SQL%20Query%20Results/max%20ticket_price.csv) |
| **10** | WAQ to extract the passengers whose route_id is 4 by improving the speed and performance of the passengers_on_flights table | [SQL](Airline%20Analysis.md#task-10-waq-to-extract-the-passengers-whose-route_id-is-4-by-improving-the-speed-and-performance-of-the-passengers_on_flights-table) | [route_id 4 passengers.csv](SQL%20Query%20Results/route_id%204%20passengers.csv) |
| **11** | WAQ to calculate the total price of all tickets booked by a customer across different aircraft IDs using rollup function | [SQL](Airline%20Analysis.md#task-11-waq-to-calculate-the-total-price-of-all-tickets-booked-by-a-customer-across-different-aircraft-ids-using-rollup-function) | [total price per customer.csv](SQL%20Query%20Results/total%20price%20per%20customer.csv) |
| **12** | WAQ to create a view with only business class customers along with the brand of airlines | [SQL](Airline%20Analysis.md#task-12-waq-to-create-a-view-with-only-business-class-customers-along-with-the-brand-of-airlines) | *(No CSV – view creation)* |
| **13** | WAQ to create a stored procedure to get the details of all passengers flying between a range of routes defined in run time. Also, return an error message if the table doesn't exist | [SQL](Airline%20Analysis.md#task-13-waq-to-create-a-stored-procedure-to-get-the-details-of-all-passengers-flying-between-a-range-of-routes-defined-in-run-time-also-return-an-error-message-if-the-table-doesnt-exist) | [passengers by route.csv](SQL%20Query%20Results/passengers%20by%20route.csv) |
| **14** | WAQ to create a stored procedure that extract all from the routes table where the travelled distance is more than 2000 miles | [SQL](Airline%20Analysis.md#task-14-waq-to-create-a-stored-procedure-that-extract-all-from-the-routes-table-where-the-travelled-distance-is-more-than-2000-miles) | [travel distance more than 2000 miles.csv](SQL%20Query%20Results/travel%20distance%20more%20than%202000%20miles.csv) |
| **15** | WAQ to create a stored procedure that groups the distance travelled by each flight into three categories | [SQL](Airline%20Analysis.md#task-15-waq-to-create-a-stored-procedure-that-groups-the-distance-travelled-by-each-flight-into-three-categories) | [roll up by row type.csv](SQL%20Query%20Results/roll%20up%20by%20row%20type.csv) |
| **16** | WAQ to extract ticket purchase date, customer id, class id, and specify if the complimentary services are provided for the specific class | [SQL](Airline%20Analysis.md#task-16-waq-to-extract-ticket-purchase-date-customer-id-class-id-and-specify-if-the-complimentary-services-are-provided-for-the-specific-class) | [complimentary service.csv](SQL%20Query%20Results/complimentary%20service.csv) |
| **17** | WAQ to extract the first record of the customer whose last name ends with Scott using a cursor from the customer table | [SQL](Airline%20Analysis.md#task-17-waq-to-extract-the-first-record-of-the-customer-whose-last-name-ends-with-scott-using-a-cursor-from-the-customer-table) | [first Scott(Name) customer.csv](SQL%20Query%20Results/first%20Scott(Name)%20customer.csv) |


