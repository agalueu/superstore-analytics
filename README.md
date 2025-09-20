# Superstore Analytics

## 📌 Overview
This project analyzes sales and profitability using the **Superstore dataset**.  
The goal is to understand sales performance, profitability, and customer trends using **PostgreSQL** and **Power BI**.

## 📊 Dataset
- **Source:** Superstore sample dataset (public, used widely in BI training)
- **Size:** ~10,000 rows (this repo includes a small sample: `data/sample_superstore.csv`)
- **Privacy:** Public, no sensitive information

## ⚙️ Tools
- PostgreSQL
- SQL (CTEs, window functions, aggregates, joins)
- Power BI (dashboards & KPIs)

## ❓ Key Business Questions
1. Which product categories and subcategories drive the most profit?
2. How do sales trends evolve monthly and regionally?
3. What customer segments are most valuable?

## 📂 Repository Structure
- `sql/` → database schema, load script, and analysis queries
- `data/` → sample dataset
- `images/` → screenshots of dashboards
- `README.md` → project summary and instructions

## 🚀 How to Reproduce
1. Create a new PostgreSQL database:
```bash
createdb superstore
