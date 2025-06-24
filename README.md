<h1 align="center">Sales Insights - Data Analysis using Tableau and SQL</h1>

This project provides Sales Insights for an India-based hardware company, developed using Tableau and SQL as part of a comprehensive data analysis workflow.

For more details on the methodology, refer to the Data Analyst Roadmap.

### About Project

- Performed India-based hardware company sales insights - A Data Analysis project.

- Developed ETL mappings using SQL to extract the data from unstructured sources and transformed it to the staging area to conduct data cleaning and design a star schema data model on Tableau.

- Developed a Tableau dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.

## Technologies Used

* Advance Excel
* MySQL | SQL Server
* Tableau | Power BI
* Statistics

## Certifications and Standards

- Data Visualization with Tableau - by Simplilearn
  
- Databases and SQL for Data Science with Python - by IBM

- Statistics for Data Science with Python - by IBM

- Data Visualization with Advanced Excel - by PWC

## Project - India based Hardware company Sales Insights

### Tableau Dashboard Link
[Tableau Dashboard - Revenue Analysis](https://public.tableau.com/views/SalesInsights-DataAnalysisProject/Dashboard-RevenueAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)

### Problem Statements
The Sales Director requires a clear view of company performance across various Indian states to optimize discount strategies.

- Q1. Revenue breakdown by cities.

- Q2. Revenue breakdown by years and months.

- Q3. Top 5 customers by revenue and sales quantity.

- Q4. Top 5 Products by revenue.
  
- Q5. Net Profit and Profit Margin by Market.

### Approach - Project Planning and Aims Grid
  
#### 1. Purpose: What? Why? What do we want to achieve?
To unlock sales insights that were previously hidden from the sales team to support decision-making and automate data gathering to reduce manual effort.

#### 2. Stakeholders: Who will be involved?
- Sales Director
- I.T. Team
- Customer Service Team
- Data and Analytics Team

#### 3. End Result: What do we want to achieve?
An automated dashboard providing quick and latest sales insights in order to support data-driven decision making.

#### 4. Success Criteria: What will be our success criteria?
- Dashboards uncovering sales order insights with the latest data available.
- Sales team able to take better decisions and prove 10% cost savings of total spend.
- Sales analysts stop data gathering manually in order to save 20% of their business time and reinvest it in value-added activity.

### Data Analysis - Approach
The project follows a structured data flow: from the source database, through ETL processes, into a data warehouse/staging area, and finally into Tableau for visualization.

### Setup Process
  
Step 1: Download the database files: db_dump.sql or db_dump.xlsx.

Step 2: Import the data into MySQL and perform ETL (Extract, Transform, Load) if required.

Step 3: Use Tableau Public or Tableau Desktop to perform the Data Analysis.
  
Step 4: Connect Tableau with the MySQL database or Excel database.
  
Step 5: Save the file as (.twb or .twbx).

## Data Analysis Using SQL
  
1. Show all customer records
    SELECT * FROM customers;

2. Show total number of customers
    SELECT count(*) FROM customers;

3. Show transactions for Chennai market (market code for Chennai is Mark001)
    SELECT * FROM transactions where market_code='Mark001';

4. Show distinct product codes that were sold in Chennai.
    SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars.
    SELECT * from transactions where currency="USD";

6. Show transactions in 2020 join by date table.
    SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
	
8. Show total revenue in year 2020, January Month.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai.
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

## Data Analysis Using Tableau 
  
### Tableau Public Dashboards: Revenue and Profit Analysis

#### Star Schema Design
The project utilizes a Star Schema in Tableau to optimize query performance and data organization, connecting fact tables with dimension tables for customers, products, and dates.

#### Tableau Dashboard - Revenue Analysis
The Revenue Analysis dashboard provides a high-level overview of total revenue, sales quantity, and revenue trends over time, broken down by market and customer segment.

#### Tableau Dashboard - Profit Analysis
The Profit Analysis dashboard focuses on bottom-line metrics, including net profit, profit margin percentage, and profit contribution by market.

## Project References

1. Tableau Project Dashboard: Sales Insights - Data Analysis using Tableau
2. MySQL Installation and Configuration
3. OLTP and OLAP Concepts
4. Star Schema: Fact Table and Dimension Table Documentation

## Related Projects

- Spotify Data Analysis using Python
- Statistics for Data Science using Python
- Python Lessons and Libraries for Data Science

---

### About the Developer

**Mohit Shyam Amode**
Data Analyst

Mohit is a professional Data Analyst with over 4 years of experience in dashboard development, SQL, and structured data analysis. He specializes in translating complex operational requirements into actionable insights using tools such as Tableau, Power BI, and Python. His expertise includes query optimization, reporting workflows, and data visualization.

**Contact Information:**
- Email: mohitshyamamode@gmail.com
- LinkedIn: linkedin.com/in/mohitamode
- GitHub: github.com/mohitamode