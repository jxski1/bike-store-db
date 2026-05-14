# bike-store-db
End-to-end database engineering project for a retail bicycle business. Includes relational schema design, data cleaning/ETL of 1,600+ records, and SQL-based business intelligence analytics. 

Project Overview
This project involves the design, implementation, and analysis of a relational database for a multi-state retail bicycle business. The goal was to transform raw, unstructured data into a functional SQL database capable of tracking sales, inventory, and customer relationships across various store locations.

Database Architecture
I architected a relational schema consisting of 9 interconnected tables. The design focuses on data normalization to reduce redundancy and ensure referential integrity through strict Primary Key (PK) and Foreign Key (FK) constraints.

Core Entities:
Sales: Orders, Order Items, Customers, Stores, and Staff.

Products: Products, Categories, and Brands.

Inventory: Stocks (linking products to specific store locations).

Technical Implementation
Data Cleaning: Processed raw datasets to standardize phone numbers, handle null values in customer records, and ensure date consistency across 1,600+ rows.

ETL Pipeline: Seperated large flat files into normalized CSVs and imported them into a MySQL environment.

Schema Design: Developed a comprehensive SQL script to automate database creation, table relations, and data dumping.

Business Intelligence (SQL Analytics)
The primary value of this database is its ability to answer complex business questions. Below are a few examples of the analytical queries I developed:

1. Revenue Trends
Calculates total revenue for each store, broken down by quarter, to identify seasonal growth.

SQL
SELECT store_name, QUARTER(order_date) as quarter, SUM(list_price * quantity) as revenue 
FROM orders ... (your query logic)
2. Inventory Management
Identifies store locations with low stock levels to trigger restock alerts.

SQL
SELECT store_name, product_name, quantity 
FROM stocks 
WHERE quantity < 5;
3. Customer Loyalty
Identifies high-value customers who have placed more than five orders for targeted marketing.

Tools Used
Language: SQL (MySQL Dialect)

Database Tool: MySQL Workbench

Data Processing: Excel / CSV transformation
