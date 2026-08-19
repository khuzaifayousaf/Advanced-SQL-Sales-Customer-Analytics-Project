📌 Project Overview :
This project focuses on Advanced Data Analytics using SQL Server, transforming transactional sales data from a structured Gold Layer into meaningful business insights.
The analysis covers sales trends, cumulative performance, year-over-year growth, category contribution, product segmentation, customer segmentation, and customer-level KPIs.
The project demonstrates practical use of advanced SQL techniques including CTEs, Window Functions, CASE statements, JOINs, aggregate functions, date functions, subqueries, and SQL Views.
________________________________________
🎯 Project Objectives :
The main objectives of this project are to:
•	Analyze sales performance over time.
•	Identify monthly and yearly sales trends.
•	Calculate cumulative sales and average prices.
•	Compare product performance across different years.
•	Identify products performing above or below their historical average.
•	Measure year-over-year sales changes.
•	Understand how different product categories contribute to total sales.
•	Segment products based on their cost.
•	Segment customers based on spending behavior and relationship lifespan.
•	Analyze customer demographics and purchasing behavior.
•	Create a reusable customer analytics report using a SQL View.
________________________________________
📊 1. Change Over Time Analysis :
The first analysis evaluates sales performance across different time periods.
Yearly Analysis
The query calculates:
•	Total Sales
•	Total Customers
•	Total Quantity
•	Yearly Sales Performance
Sales are grouped by the year of the order date to identify long-term business trends.
Monthly Analysis
Monthly performance is analyzed using multiple SQL approaches:
•	YEAR() + MONTH()
•	DATETRUNC()
•	FORMAT()
This demonstrates different ways to perform date-based aggregation in SQL Server.
Business Questions
•	How are sales changing over time?
•	Which years generated the highest sales?
•	Which months performed best?
•	How does sales volume change across different periods?
________________________________________
📈 2. Cumulative Analysis :
The project applies SQL Window Functions to calculate cumulative metrics.
Metrics
•	Running Total Sales
•	Average Price
•	Moving Average
The analysis uses:
•	SUM() OVER()
•	AVG() OVER()
•	PARTITION BY
•	ORDER BY
•	Window frame definitions
Purpose
Cumulative analysis helps understand how sales accumulate over time and provides a better view of overall performance trends.
________________________________________
📅 3. Year-over-Year Performance Analysis :
The project analyzes yearly product performance by comparing each product's sales with:
•	Its average yearly sales
•	Previous year's sales
•	Difference from previous year
•	Performance direction
A CTE (Common Table Expression) is first used to calculate yearly product sales.
Key Calculations
Average Sales
Calculates the average yearly sales for each product.
Tracking Sales
Measures the difference between yearly sales and the product's average sales.
Performance Categorization
Products are categorized as:
•	Above Average
•	Below Average
•	Average
Previous Year Sales
The LAG() function retrieves the previous year's sales.
Year-over-Year Difference
Calculates the change in sales compared with the previous year.
Performance Flag
Products are classified as:
•	Increasing
•	Decreasing
•	No Change
Business Questions
•	Which products are improving?
•	Which products are declining?
•	Which products consistently perform above average?
•	How much did sales change compared with the previous year?
________________________________________
🥧 4. Part-to-Whole Analysis :
This analysis determines how much each product category contributes to overall sales.
Metrics
•	Category Sales
•	Overall Sales
•	Category Contribution %
•	Category Ranking
The analysis uses the window function:
SUM(Total_Sales) OVER()
to calculate total company sales and determine each category's percentage contribution.
Business Questions
•	Which category contributes the most revenue?
•	What percentage of total sales comes from each category?
•	Which categories have the largest business impact?
________________________________________
📦 5. Product Segmentation :
Products are segmented according to their product cost.
Product Cost Segments
Cost Range	Segment
< 100	Below 100
100–500	100–500
500–1000	500–1000
> 1000	Above 1000
A CASE statement is used to assign each product to a cost segment.
The final analysis calculates the number of products within each segment.
Business Questions
•	How many products fall into each cost range?
•	What is the distribution of the product portfolio?
•	Which cost segment contains the most products?
________________________________________
👥 6. Customer Segmentation :
Customers are segmented according to their spending behavior and relationship lifespan.
Customer Segments
VIP Customer
•	Spending > $5,000
•	Customer lifespan ≥ 12 months
Regular Customer
•	Spending ≤ $5,000
•	Customer lifespan ≥ 12 months
New Customer
•	Customer lifespan < 12 months
Customer Metrics
The analysis calculates:
•	First Order Date
•	Last Order Date
•	Total Sales
•	Customer Lifespan
•	Customer Segment
Business Questions
•	How many VIP customers exist?
•	How many regular customers exist?
•	How many customers are new?
•	Which customer segment represents the largest group?
________________________________________
👤 7. Customer Report View :
A reusable SQL View named:
gold.customer_report
is created to consolidate customer-level information and KPIs.
The view combines transactional information from the Sales Fact table with customer information from the Customer Dimension.
Customer Information
The report includes:
•	Customer Key
•	Customer Name
•	Full Name
•	Age
•	Age Category
•	Customer Category
Customer Behavioral Metrics
•	Total Orders
•	Total Sales
•	Total Quantity Purchased
•	Total Products Purchased
•	Customer Lifespan
•	Recency
Customer KPIs
Average Order Value (AOV)
Measures the average amount spent per order.
Average Monthly Spend
Measures the customer's average spending per month during their relationship period.
Recency
Measures the number of months since the customer's most recent order.
________________________________________
🧮 8. Customer Age Segmentation :
Customers are also grouped into age categories:
•	Under 20
•	20–29
•	30–39
•	40–49
•	50 and Above
This allows customer purchasing behavior to be analyzed across different demographic groups.
________________________________________
🛠️ SQL Techniques Used :
This project demonstrates practical use of:
•	SELECT
•	WHERE
•	GROUP BY
•	ORDER BY
•	LEFT JOIN
•	CASE
•	CTE
•	SUM()
•	AVG()
•	COUNT()
•	COUNT(DISTINCT)
•	SUM() OVER()
•	AVG() OVER()
•	LAG()
•	YEAR()
•	MONTH()
•	DATEDIFF()
•	DATETRUNC()
•	FORMAT()
•	CONCAT()
•	CAST()
•	ROUND()
•	SQL Views
•	Window Functions
•	Aggregate Functions
•	Date Functions
________________________________________
🗂️ Data Model :
The analysis uses a Gold Layer structure containing key tables such as:
gold.sales_fact
Contains transactional sales information including:
•	Sales Order Number
•	Order Date
•	Customer Key
•	Product Key
•	Price
•	Quantity
•	Sales
gold.product_dim
Contains product-related information such as:
•	Product Key
•	Product Name
•	Product Category
•	Product Cost
gold.customer_dim
Contains customer-related information such as:
•	Customer Key
•	Customer Name
•	First Name
•	Last Name
•	Birth Date
The fact and dimension tables are connected using their respective keys to perform analytical queries.
________________________________________
📌 Key Business Insights Enabled :
This project enables businesses to understand:
•	Overall sales growth and trends.
•	Monthly and yearly sales performance.
•	Product-level performance changes.
•	Increasing and declining products.
•	Category revenue contribution.
•	Product cost distribution.
•	Customer value and spending behavior.
•	Customer retention and recency.
•	Customer lifecycle and segmentation.
•	Average customer order value.
•	Average monthly customer spending.
________________________________________
🚀 Skills Demonstrated :
SQL Server | Advanced SQL | Data Analysis | Business Analytics | Sales Analytics | Customer Analytics | Data Segmentation | Performance Analysis | Window Functions | CTEs | SQL Views | KPI Development | Data Transformation
________________________________________
📁 Project Outcome :
The project converts raw transactional data into a structured analytical reporting layer, providing both high-level business performance analysis and detailed customer-level insights.
It demonstrates how SQL can be used not only for querying data, but also for performing advanced business analysis and developing reusable analytical datasets for reporting and BI dashboards.


