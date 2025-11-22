# Airline-Analysis---SQL

### Project Overview
This project simulates a real-world database management scenario for an aviation company named Air Cargo, which offers both passenger and freight services through partnerships with other airlines. The objective is to analyze air travel data to improve operational efficiency, optimize route planning, and enhance the customer experience.

### Insights
- Datasets can be found [here](1697127247_airlines_datasets/)
- SQL Queries can be found [here](Airline%20Analysis.sql/)
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
- Display all the passengers/customers who have travelled in routes 01 to 25.
- Identify the number of passengers and total revenue in Business Class.
- Display the full name of customers.
- Extract the customers who have registered and booked a ticket.
- Identify the customer's first name and last name based on their ID and airline brand 'Emirates'.
- Identify the customers who have travelled by 'Economy Plus' class.
- Identify whether the revenue has crossed 10000 or not.
- Find the maximum ticket price for each class.
- Extract the passengers whose route ID is 4.
- Calculate the total price of all tickets booked by a customer across different aircraft IDs.
- Create a view with only business class customers along with the brand of airline.
- Create a stored procedure to get the details of all passengers flying between a range of routes defined in run time. Also, return an error message if the table doesn't exist.
- Create a stored procedure that extracts all the details from the routes table where the travelled distance is more than 2000 miles.
- Create a stored procedure that groups the distance travelled by each flight into three categories. The categories are, short distance travel (SDT) for >=0 AND <= 2000 miles, intermediate distance travel (IDT) for >2000 AND <=6500, and long-distance travel (LDT) for >6500.
- Extract ticket purchase date, customer ID, class ID and specify if the complimentary services are provided for the specific class. Condition: If the class is Business and Economy Plus, then complimentary services are given as Yes, else it is No.
- Extract the first record of the customer whose last name ends with Scott using a cursor.

