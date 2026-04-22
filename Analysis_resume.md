# 📊 Analysis Summary

This section explains the analytical approach used in the queries from `sql/Analysis.sql` and highlights the key business insights derived from the data.

---

# 1. Profit Hotspot

### 📝 Purpose
This analysis reveals how profitability varies across regions and customer segments.

### ⚙️ Approach
- Aggregated total sales and profit by region and segment
- Calculated profit margin (%) to evaluate efficiency
- Ranked results to identify top and bottom performers

### 📊 Business Insight
This analysis highlights which region–segment combinations generate the highest profitability. It can support strategic decisions such as targeting high-margin segments or optimizing pricing and discount strategies in underperforming areas.

---

# 2. Total Sales per Product

### 📝 Purpose
This analysis identifies top-performing products over time.

### ⚙️ Approach
- Joined products, orders, and order_details tables
- Aggregated total sales by product and year
- Ranked products based on sales performance

### 📊 Business Insight
This analysis reveals both consistent bestsellers and products with fluctuating demand. It supports decisions related to inventory planning, product strategy, and targeted promotions.

---

# 3. Sales Trends by Category (YoY Growth)

### 📝 Purpose
This analysis reveals how sales evolve over time by category.

### ⚙️ Approach
- Aggregated yearly sales by category
- Used LAG() to compare current vs previous year
- Calculated year-over-year (YoY) growth (%)

### 📊 Business Insight
This analysis helps identify high-growth categories, stable performers, and declining segments, enabling better strategic planning and resource allocation.

---

# 4. YoY Growth and Ranking Dynamics

### 📝 Purpose
This analysis evaluates category performance across regions over time, including growth trends and ranking changes.

### ⚙️ Approach
- Calculated total sales and profit by category, region, and year
- Applied ranking functions to identify top performers
- Computed YoY growth for both sales and profit
- Measured ranking changes using window functions

### 📊 Business Insight
This analysis provides a comprehensive view of performance by:
- Identifying dominant categories in each region
- Tracking growth trends over time
- Highlighting categories gaining or losing competitive position

---

# 5. Top-Selling Category per Year

### 📝 Purpose
This analysis identifies the leading category in each year based on total sales.

### ⚙️ Approach
- Aggregated total sales by category and year
- Applied DENSE_RANK() to rank categories within each year
- Selected the top-ranked category

### 📊 Business Insight
This analysis reveals shifts in category dominance over time, helping track market trends and guide long-term investment decisions.

---

# 6. Category Performance by Region

### 📝 Purpose
This analysis compares category performance across regions.

### ⚙️ Approach
- Aggregated sales and profit by category, region, and year
- Applied ranking functions to evaluate performance

### 📊 Business Insight
This analysis highlights regional differences in category performance, helping identify where certain categories perform strongly or require strategic adjustments.

---

# 7. Customer Segment Value Analysis

### 📝 Purpose
This analysis evaluates the value of customer segments within each region.

### ⚙️ Approach
- Aggregated total sales and profit by region and segment
- Calculated profit margin (%)
- Ranked segments based on sales, profit, and margin
- Combined rankings into a composite performance score

### 📊 Business Insight
This analysis identifies the most valuable customer segments by balancing revenue, profitability, and efficiency. It supports targeted marketing strategies and resource prioritization.

---

## 📌 Final Insight

Overall, this analysis demonstrates how combining structured SQL modeling with window functions and aggregations enables deeper visibility into business performance, supporting data-driven decision-making across products, regions, and customer segments.
