# Online-Retail-SQL-and-Tableau-Project
A project where a online retail dataset is taken into Microsoft SQL for cleaning and transforming to be analysed and eventually fed into Tableau for visual insights.


This is a summary of what I have done in this project, the outputs produced, the tools I have used and the skills I have demonstrated:

Online Retail II – SQL Analytics Project
This project uses the Online Retail II transactional dataset to build a small analytical data model entirely in SQL before visualising results in Tableau.
The starting point was a raw CSV containing transactional invoice data. Rather than cleaning in Excel, all transformation and validation was handled inside SQL to simulate a realistic data workflow.
Data preparation included:
•	Removing cancelled invoices
•	Excluding negative quantities (returns)
•	Filtering out null CustomerID values
•	Creating a Revenue column (Quantity * UnitPrice)
•	Standardising dates to month-level granularity
•	Ensuring duplicate handling at invoice-product level
From this cleaned base table, multiple analytical tables were created.
Customer summary table (1 row per customer):
•	First purchase date
•	Most recent purchase date
•	Total orders
•	Total revenue
•	Average order value
Monthly performance table (1 row per month):
•	Total revenue
•	Distinct active customers
•	Order volume
Cohort retention table:
•	Cohort month (customer’s first purchase month)
•	Activity month
•	Month index (months since first purchase)
•	Active customers per cohort
•	Retention rate calculated against Month 0
RFM segmentation table:
•	Recency (days since last purchase)
•	Frequency (distinct invoices)
•	Monetary value (total spend)
•	Segmentation scoring logic
The project required extensive use of:
•	CTEs for multi-stage transformations
•	Self-joins
•	Date difference calculations
•	Aggregations and distinct counts
•	Window functions
•	Derived metrics
•	Structured query layering
The cohort analysis identifies customer decay curves and allows estimation of lifetime value behaviour. Monthly aggregation highlights seasonality and revenue volatility. RFM segmentation separates high-value customers from low-engagement segments.
All Tableau dashboards were built on curated SQL outputs rather than raw CSV data. This demonstrates separation of data preparation from visualisation and reflects real-world BI workflow.
Overall, the project shows the ability to take raw transactional data and turn it into commercially meaningful outputs using structured SQL logic.
