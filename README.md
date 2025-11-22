# Airline-Analysis---MySQL DBA Tasks ✈️ 

### Project Overview
This project simulates a real-world database management scenario for an aviation company named **Air Cargo**, which offers both passenger and freight services through partnerships with other airlines. The objective is to analyze air travel data to improve operational efficiency, optimize route planning, and enhance the customer experience.

### Insights
- **Datasets:** All raw airline datasets are available [here](1697127247_airlines_datasets/).  
- **SQL Queries:** The complete SQL scripts for all tasks can be accessed [here](Airline%20Analysis.md).  
- **Query Results:** The output of SQL queries, in CSV format, is available [here](SQL%20Query%20Results/).

### Business Problem
Air Cargo wants to gain deeper insights into its operations by identifying:
- Regular passengers (to offer loyalty benefits)
- Busiest routes (to better allocate aircraft)
- Ticket sales patterns (to improve revenue and pricing strategy).

### DBA Tasks - SQL Queries  Overview

As a DBA you need to perform the following operations:

| Task # | Task | SQL Query | Result CSV |
|--------|------|-------|------------|
| 1 | Display passengers in routes 01–25 | [Query](Airline%20Analysis.md#task-1-display-passengers-in-routes-01-25) | [route 01-25.csv](SQL%20Query%20Results/route%2001-25.csv) |
| 2 | Business class revenue summary | [Query](Airline%20Analysis.md#task-2-business-class-revenue-summary) | [total revenue.csv](SQL%20Query%20Results/total%20revenue.csv) |
| 3 | Customer full names | [Query](Airline%20Analysis.md#task-3-customer-full-names) | [customers full name.csv](SQL%20Query%20Results/customers%20full%20name.csv) |
| 4 | Registered & booked customers | [Query](Airline%20Analysis.md#task-4-registered--booked-customers) | [registered customers.csv](SQL%20Query%20Results/registered%20customers.csv) |
| 5 | Emirates customer names | [Query](Airline%20Analysis.md#task-5-emirates-customer-names) | [Emirates Customers.csv](SQL%20Query%20Results/Emirates%20Customers.csv) |
| 6 | Economy Plus travellers | [Query](Airline%20Analysis.md#task-6-economy-plus-travellers) | [Economy_Plus Class Passengers.csv](SQL%20Query%20Results/Economy_Plus%20Class%20Passengers.csv) |
| 7 | Revenue > 10000 check | [Query](Airline%20Analysis.md#task-7-revenue-greater-than-10000-check) | [Revenue more than 10000.csv](SQL%20Query%20Results/Revenue%20more%20than%2010000.csv) |
| 8 | Create & grant user access | [Query](Airline%20Analysis.md#task-8-create--grant-user-access) | *(No CSV)* |
| 9 | Max ticket price per class | [Query](Airline%20Analysis.md#task-9-max-ticket-price-per-class) | [max ticket_price.csv](SQL%20Query%20Results/max%20ticket_price.csv) |
| 10 | Passengers with route_id 4 | [Query](Airline%20Analysis.md#task-10-passengers-with-route_id-4) | [route_id 4 passengers.csv](SQL%20Query%20Results/route_id%204%20passengers.csv) |
| 11 | Total tickets price per customer | [Query](Airline%20Analysis.md#task-11-total-tickets-price-per-customer) | [total price per customer.csv](SQL%20Query%20Results/total%20price%20per%20customer.csv) |
| 12 | Business class view | [Query](Airline%20Analysis.md#task-12-business-class-view) | *(No CSV)* |
| 13 | Stored procedure: passengers by route | [Query](Airline%20Analysis.md#task-13-stored-procedure-passengers-by-route) | [passengers by route.csv](SQL%20Query%20Results/passengers%20by%20route.csv) |
| 14 | Stored procedure: routes > 2000 miles | [Query](Airline%20Analysis.md#task-14-stored-procedure-routes-more-than-2000-miles) | [travel distance more than 2000 miles.csv](SQL%20Query%20Results/travel%20distance%20more%20than%202000%20miles.csv) |
| 15 | Categorize flight distance | [Query](Airline%20Analysis.md#task-15-categorize-flight-distance) | [roll up by row type.csv](SQL%20Query%20Results/roll%20up%20by%20row%20type.csv) |
| 16 | Complimentary service per class | [Query](Airline%20Analysis.md#task-16-complimentary-service-per-class) | [complimentary service.csv](SQL%20Query%20Results/complimentary%20service.csv) |
| 17 | First customer with last name Scott | [Query](Airline%20Analysis.md#task-17-first-customer-with-last-name-scott) | [first Scott(Name) customer.csv](SQL%20Query%20Results/first%20Scott(Name)%20customer.csv) |

### Conclusion – Executive Summary

The Airline Analysis project reveals actionable insights for Air Cargo:  

- **High-demand routes & classes:** Routes 01–25 and Economy Plus are the most traveled, highlighting key revenue corridors.  
- **Revenue drivers:** Business class is a significant contributor to overall revenue, with some routes exceeding $10,000 in sales.  
- **Customer segmentation:** Identifying frequent flyers, registered customers, and brand-specific travelers (Emirates) enables targeted loyalty programs.  
- **Operational efficiency:** Total spend per customer, max ticket prices, and route-specific passenger counts support optimized resource allocation and route planning.  
- **Service offerings:** Complimentary services for Business and Economy Plus enhance customer satisfaction and marketing opportunities.  

**Takeaway:** Structured data management and targeted analysis allow Air Cargo to make informed decisions, improve revenue, and enhance the passenger experience.  



