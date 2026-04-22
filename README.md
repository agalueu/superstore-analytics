# 🛒 Superstore Sales & Profitability Analysis

## 📌 Overview
This project analyzes sales performance, profitability, and customer behavior using the Superstore dataset.

The objective is to identify key revenue drivers, evaluate profitability patterns, and understand how customer segments and regions contribute to overall business performance.

The analysis is performed using PostgreSQL for data modeling and SQL analytics, with Power BI used for visualization and storytelling.

---

## 📊 Dataset
- Source: Public Superstore dataset (commonly used in BI and analytics training)
- Size: ~10,000 rows
- Contents: Orders, customers, products, sales, discounts, and profit
- Privacy: No sensitive data

---

## ⚙️ Tools & Technologies
- PostgreSQL
- SQL (CTEs, window functions, aggregations, joins)
- Power BI

---

## ❓ Key Business Questions
1. What are the top-performing products by sales over time?
2. Which categories drive the most profit across regions?
3. How do sales trends evolve year over year by category?
4. How do sales and profit growth (YoY) change across regions and categories?
5. Which customer segments are the most valuable within each region?

---

## 🧱 Data Modeling

The raw dataset was normalized into a relational schema to improve data consistency, scalability, and query performance:

- `customers` → customer information and segmentation
- `orders` → order-level data
- `products` → product catalog
- `order_details` → transactional line items (sales, quantity, profit)

### Relationships:
- One customer → many orders  
- One order → many products (via order_details)

---

## 📂 Repository Structure
- `docs/` → ERD and raw dataset
- `images/` → Power BI dashboards and query outputs
- `sql/`
  - `SCHEMA.sql` → schema creation and data loading
  - `Analysis.sql` → analytical queries
- `Analysis_resume.md` → analysis explanations and insights
- `README.md` → project documentation

---

## 🔄 How to Reproduce

1. Create a PostgreSQL database  
2. Run `sql/SCHEMA.sql` to:
   - Create tables  
   - Load and normalize data  
3. Run queries from `sql/Analysis.sql`  
4. (Optional) Connect Power BI to PostgreSQL for visualization  

---

## 📊 Dashboard Highlights

The Power BI dashboard focuses on:

- Sales and profit distribution by category and region  
- Profitability hotspots (region × segment)  
- Year-over-year growth trends  
- Ranking dynamics across categories  
- Top-performing products and categories over time  

---

## ✅ Key Insights

- Sales performance varies significantly across regions and categories.  
- Technology consistently drives high profitability.  
- Some subcategories (e.g., Tables) generate negative profit despite strong sales.  
- Profitability is not always aligned with revenue, highlighting pricing and discount inefficiencies.  

---

## 📌 Key Takeaway

This project demonstrates how structured SQL modeling combined with analytical techniques (window functions, aggregations, ranking) can transform raw transactional data into actionable business insights that support data-driven decision-making.
