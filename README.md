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

| Task # | Task | SQL | Result CSV |
|--------|------|-----|------------|
| 1 | Display passengers in routes 01–25 | [SQL](Airline%20Analysis.md#task-1-display-passengers-in-routes-01-25) | [route 01-25.csv](SQL%20Query%20Results/route%2001-25.csv) |
| 2 | Business class revenue summary | [SQL](Airline%20Analysis.md#task-2-business-class-revenue-summary) | [total revenue.csv](SQL%20Query%20Results/total%20revenue.csv) |
| 3 | Customer full names | [SQL](Airline%20Analysis.md#task-3-customer-full-names) | [customers full name.csv](SQL%20Query%20Results/customers%20full%20name.csv) |
| 4 | Registered & booked customers | [SQL](Airline%20Analysis.md#task-4-registered--booked-customers) | [registered customers.csv](SQL%20Query%20Results/registered%20customers.csv) |
| 5 | Emirates customer names | [SQL](Airline%20Analysis.md#task-5-emirates-customer-names) | [Emirates Customers.csv](SQL%20Query%20Results/Emirates%20Customers.csv) |
| 6 | Economy Plus travellers | [SQL](Airline%20Analysis.md#task-6-economy-plus-travellers) | [Economy_Plus Class Passengers.csv](SQL%20Query%20Results/Economy_Plus%20Class%20Passengers.csv) |
| 7 | Revenue > 10000 check | [SQL](Airline%20Analysis.md#task-7-revenue-10000-check) | [Revenue more than 10000.csv](SQL%20Query%20Results/Revenue%20more%20than%2010000.csv) |
| 8 | Create & grant user access | [SQL](Airline%20Analysis.md#task-8-create--grant-user-access) | *(No CSV)* |
| 9 | Max ticket price per class | [SQL](Airline%20Analysis.md#task-9-max-ticket-price-per-class) | [max ticket_price.csv](SQL%20Query%20Results/max%20ticket_price.csv) |
| 10 | Passengers with route_id 4 | [SQL](Airline%20Analysis.md#task-10-passengers-with-route_id-4) | [route_id 4 passengers.csv](SQL%20Query%20Results/route_id%204%20passengers.csv) |
| 11 | Total tickets price per customer | [SQL](Airline%20Analysis.md#task-11-total-tickets-price-per-customer) | [total price per customer.csv](SQL%20Query%20Results/total%20price%20per%20customer.csv) |
| 12 | Business class view | [SQL](Airline%20Analysis.md#task-12-business-class-view) | *(No CSV)* |
| 13 | Stored procedure: passengers by route | [SQL](Airline%20Analysis.md#task-13-stored-procedure-passengers-by-route) | [passengers by route.csv](SQL%20Query%20Results/passengers%20by%20route.csv) |
| 14 | Stored procedure: routes > 2000 miles | [SQL](Airline%20Analysis.md#task-14-stored-procedure-routes->-2000-miles) | [travel distance more than 2000 miles.csv](SQL%20Query%20Results/travel%20distance%20more%20than%202000%20miles.csv) |
| 15 | Categorize flight distance | [SQL](Airline%20Analysis.md#task-15-categorize-flight-distance) | [roll up by row type.csv](SQL%20Query%20Results/roll%20up%20by%20row%20type.csv) |
| 16 | Complimentary service per class | [SQL](Airline%20Analysis.md#task-16-complimentary-service-per-class) | [complimentary service.csv](SQL%20Query%20Results/complimentary%20service.csv) |
| 17 | First customer with last name Scott | [SQL](Airline%20Analysis.md#task-17-first-customer-with-last-name-scott) | [first Scott(Name) customer.csv](SQL%20Query%20Results/first%20Scott(Name)%20customer.csv) |

