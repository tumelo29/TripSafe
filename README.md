🚗 TripSafe: South African Ride-Hailing Data Analysis & Database System
A comprehensive relational database and analytical reporting project built for CMPG321 (Phase 1 & Phase 2). This project investigates trip cancellations, safety metrics, and fleet quality across major urban centers in South Africa using ride-hailing operational data (Uber & Bolt).
🚀 Project Overview
TripSafe models the complete lifecycle of 50,000 ride-hailing trips. It combines transactional data, fare breakdowns, surge pricing zones, rider demographics, driver profiles, vehicle specifications, and user reviews into a robust relational database to uncover actionable operational insights.
📊 Key Features & Analysis
￼ Cancellation Pattern Analysis: Evaluates cancellation reasons across 7 South African cities using window functions and conditional aggregation.
￼ Surge Pricing Friction: Investigates the monotonic relationship between surge multipliers (1.0x to 2.1x+) and trip cancellation spikes.
￼ Fleet & Vehicle Quality Control: Analyzes how vehicle age, make, and category tiers correlate with trip disruptions.
￼ Safety & Service Quality Tracking: Assesses driver rating tiers and safety concern flags by region.
￼ Financial Impact Modeling: Estimates potential fare revenue associated with cancellations using Common Table Expressions (CTEs) and subqueries.
￼ Database Optimization & Transactions: Demonstrates ACID compliance with ⁠START TRANSACTION⁠ / ⁠ROLLBACK⁠ and query performance tuning using ⁠EXPLAIN⁠ and composite indexing.
🛠️ Tech Stack & Advanced SQL Techniques
￼ Database Management System: MySQL 8.0
￼ Advanced SQL Constructs:
￼ Multi-table ⁠INNER⁠ and ⁠LEFT⁠ Joins
￼ Conditional Aggregation (⁠CASE⁠ statements)
￼ Window Functions (⁠RANK()⁠, ⁠SUM() OVER (PARTITION BY)⁠)
￼ Common Table Expressions (CTEs) & Inline Views
￼ Transaction Control (⁠START TRANSACTION⁠, ⁠COMMIT⁠, ⁠ROLLBACK⁠)
￼ Query Performance Optimization (⁠EXPLAIN⁠, ⁠CREATE INDEX⁠)
🗄️ Database Schema Structure
The ⁠uberbolt⁠ database consists of 7 normalized relational tables:
1. ⁠pricing_surge_zones⁠ — Regional base fares and per-km/min tariffs across 9 zones.
2. ⁠sa_riders⁠ — Rider demographics, home cities, and preferred payment methods.
3. ⁠sa_drivers⁠ — Driver profiles, ratings, platform affiliations (Uber/Bolt), and tenure.
4. ⁠vehicles⁠ — Vehicle specifications linked 1:1 to drivers (make, model, year, category).
5. ⁠trip_headers⁠ — Central transactional table tracking requests, timestamps, statuses, and cancellation reasons.
6. ⁠trip_fare_breakdown⁠ — Distance, duration, surge multipliers, tolls, tips, and fare splits.
7. ⁠trip_reviews⁠ — Rider/driver ratings and feedback comment themes.
💻 How to Run the Database Script

Clone the repository:
git clone https://github.com/tumelo29/TripSafe-Project.git
Open MySQL Workbench or your preferred MySQL 8.0 client.
Execute the database creation and loading script (Appendix A script) to build the schema, constraints, and import the CSV datasets using LOAD DATA LOCAL INFILE.
Run the analytical queries (Appendix B script) to reproduce the findings and visual reports.
