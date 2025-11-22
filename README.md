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
|--------|-----------------|-----------|------------|
| **1** | Passengers who travelled in routes 01–25 | [SQL](Airline%20Analysis.md--##Task-1-WAQ-to-display-all-the-passengers-(customers)-who-have-travelled-in-routes-01-to-25.) | [route 01-25.csv](SQL%20Query%20Results/route%2001-25.csv) |
| **2** | Number of passengers & total revenue in Business Class | [SQL](Airline%20Analysis.md#task-2-number-of-passengers--total-revenue-in-business-class) | [total revenue.csv](SQL%20Query%20Results/total%20revenue.csv) |
| **3** | Display full name of customers | [SQL](Airline%20Analysis.md#task-3-display-full-name-of-customers) | [customers full name.csv](SQL%20Query%20Results/customers%20full%20name.csv) |
| **4** | Customers who registered AND booked a ticket | [SQL](Airline%20Analysis.md#task-4-customers-who-registered-and-booked-a-ticket) | [registered customers.csv](SQL%20Query%20Results/registered%20customers.csv) |
| **5** | First & last name of customers flying Emirates | [SQL](Airline%20Analysis.md#task-5-first--last-name-of-customers-flying-emirates) | [Emirates Customers.csv](SQL%20Query%20Results/Emirates%20Customers.csv) |
| **6** | Customers who travelled by Economy Plus class | [SQL](Airline%20Analysis.md#task-6-customers-who-travelled-by-economy-plus-class) | [Economy_Plus Class Passengers.csv](SQL%20Query%20Results/Economy_Plus%20Class%20Passengers.csv) |
| **7** | Check if revenue has crossed 10000 | [SQL](Airline%20Analysis.md#task-7-check-if-revenue-has-crossed-10000) | [Revenue more than 10000.csv](SQL%20Query%20Results/Revenue%20more%20than%2010000.csv) |
| **8** | Create a new user and grant access to database | [SQL](Airline%20Analysis.md#task-8-create-a-new-user-and-grant-access-to-database) | *(No CSV – administrative task)* |
| **9** | Maximum ticket price for each class | [SQL](Airline%20Analysis.md#task-9-maximum-ticket-price-for-each-class) | [max ticket_price.csv](SQL%20Query%20Results/max%20ticket_price.csv) |
| **10** | Passengers whose route ID is 4 | [SQL](Airline%20Analysis.md#task-10-passengers-whose-route-id-is-4) | [route_id 4 passengers.csv](SQL%20Query%20Results/route_id%204%20passengers.csv) |
| **11** | Total price of all tickets booked by each customer | [SQL](Airline%20Analysis.md#task-11-total-price-of-all-tickets-booked-by-each-customer) | [total price per customer.csv](SQL%20Query%20Results/total%20price%20per%20customer.csv) |
| **12** | View with Business Class customers + airline brand | [SQL](Airline%20Analysis.md#task-12-view-with-business-class-customers--airline-brand) | *(No CSV – view creation)* |
| **13** | Stored procedure: passengers flying between route range | [SQL](Airline%20Analysis.md#task-13-stored-procedure-passengers-flying-between-route-range) | [passengers by route.csv](SQL%20Query%20Results/passengers%20by%20route.csv) |
| **14** | Stored procedure: routes with travelled distance > 2000 miles | [SQL](Airline%20Analysis.md#task-14-stored-procedure-routes-with-travelled-distance-2000-miles) | [travel distance more than 2000 miles.csv](SQL%20Query%20Results/travel%20distance%20more%20than%202000%20miles.csv) |
| **15** | Stored procedure: categorize distance (SDT, IDT, LDT) | [SQL](Airline%20Analysis.md#task-15-stored-procedure-categorize-distance-sdt-idt-ldt) | [roll up by row type.csv](SQL%20Query%20Results/roll%20up%20by%20row%20type.csv) |
| **16** | Complimentary service indicator by class | [SQL](Airline%20Analysis.md#task-16-complimentary-service-indicator-by-class) | [complimentary service.csv](SQL%20Query%20Results/complimentary%20service.csv) |
| **17** | First customer whose last name ends with “Scott” (cursor) | [SQL](Airline%20Analysis.md#task-17-first-customer-whose-last-name-ends-with-scott-cursor) | [first Scott(Name) customer.csv](SQL%20Query%20Results/first%20Scott(Name)%20customer.csv) |


