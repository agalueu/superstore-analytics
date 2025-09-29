# Superstore Analytics

## 📌 Overview
This project analyzes sales and profitability using the **Superstore dataset**.  
The goal is to understand sales performance, profitability, and customer trends using **PostgreSQL** and **Power BI**.

## 📊 Dataset
- **Source:** Superstore sample dataset (public, used widely in BI training)
- **Size:** ~10,000 rows (this repo includes the file used for this project: `superstore.csv`)
- **Privacy:** Public, no sensitive information

## ⚙️ Tools
- PostgreSQL
- SQL (CTEs, window functions, aggregates, joins)
- Power BI (dashboards & KPIs)

## ❓ Key Business Questions
1. Which are the total sales per product?
2. Which product categories and subcategories drive the most profit?
3. How do sales trends by category?
4. how YoY growth by sales and profit have changed over the years based on product´s category?
5. What customer segments and region combined are most valuable?

## 📂 Repository Structure
- docs/                  → ERD & raw dataset files
- images/                → screenshots of dashboards (Power BI) and query results (pgAdmin)
- sql/                   → database schema, load script, and analysis queries
- Analysis_resume.md     → All queries analysis used for this repository
- README.md              → project summary and instructions 


## Database Schema & ERD

The data is normalized into these tables:

- `customers` (customer info + region etc.)  
- `orders` (order-level info)  
- `products` (product catalog)  
- `order_details` (line-item level: sales, quantity, profit etc.)

**Relationships:**

- Each `order` links to one customer.  
- `order_details` links orders to products (many-to-many through that table).  


**Entity Relationship Diagram (ERD):**

![ERD](docs/ERD.png)

## 🔄 How to Reproduce
- Create a PostgreSQL database:
      * In pgAdmin → right-click Databases → Create - Database → name it `superstore` (or any name you preffer).
- Schema & Data Import:
      * Run the schema script in [SCHEMA](sql/SCHEMA.sql) to create all tables and insert data.
- Sample queries:
      * Analytical SQL queries are available in [Analysis](sql/Analysis.sql).
      * These queries can be run in pgAdmin or connected directly to Power BI for visualization.

## 📊 Power BI Integration
For the visualization layer, I connected Power BI directly to PostgreSQL:

- All SQL queries were first developed and validated in **pgAdmin**.  
- Using the native PostgreSQL connector, these queries were imported into Power BI.  
- This workflow allowed me to rely on **SQL for all data modeling and transformations**, keeping Power BI focused on the **visualization and storytelling** aspects.  


## Images shared
- Example or query and results from top selling category [Highlight top selling category](images/Highlight_top_selling_category.png)
- Example of profit hotspot [Profit Hotspot](images/profit_hotspot.png)
- Ready chart on powerBI sammple of some queries into 2 different images
     * superstore sales analysis **** [Superstore Analysis](images/superstore_analysis.png)
       In this one we see a overall profitability of the "company" or in this case the superstore database
     * superstore sales analisys 2 **** [Superstore Analysis 2](images/superstore_analysis_2.png)
       we can see on this image some interesting charts on how the rank changes over the years by profit and sales, that rank changes can be usefull for the impact it has on sellings
       the higher number on rank means the low selling products for example or less sales.
       We can see same for YoY growth by profit and sales and a overall top sellers each year.

## Queries analysis and insights from the project
For detailed SQL queries and insights, see [Analysis Resume](Analysis_resume.md)
