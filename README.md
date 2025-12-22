# Advanced-Retail-Analytics-Strategic-Business-Intelligence
An end-to-end data analytics project focused on performing advanced SQL analysis on a retail dataset. The project uses a "Gold Layer" architecture, where raw data is transformed into specialized views for reporting and strategic decision-making.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
---

# Project Title: Advanced Retail Analytics & Strategic Business Intelligence

**Domain:** E-Commerce / Global Retail

**Tools:** SQL Server (T-SQL), Window Functions, Data Modeling (Star Schema)

## 1. Project Overview & Business Problem

### The "Growth-Retention" Paradox

A global retail enterprise is experiencing high transactional volume but lacks deep visibility into customer behavior and product performance. The management is unable to differentiate between seasonal spikes and long-term growth, nor can they identify which customer segments drive the highest **Lifetime Value (CLV)**.

**Objective:**
To build a robust, end-to-end analytical framework that transforms raw data into a "Gold Layer" of actionable insights. This project focuses on:

* **Customer Lifecycle Management:** Identifying VIPs vs. Churn risks.
* **Product Performance Dynamics:** Segmenting the catalog into high and low performers.
* **Time-Series Forecasting:** Benchmarking Year-over-Year (YoY) growth and cumulative sales trends.

---

## 2. Data Architecture (The "Gold Layer")

The project follows a modular architecture where raw data is cleaned and joined into three primary entities:

* **`gold.fact_sales`**: The core transactional table containing order dates, quantities, and sales amounts.
* **`gold.dim_customers`**: Enriched demographic data including customer age, location, and account creation dates.
* **`gold.dim_products`**: Product-level details including manufacturing costs, categories (Bikes, Clothing, Accessories), and subcategories.

---

## 3. Detailed Technical Implementation

### A. Customer Intelligence & Segmentation

Using advanced logic, customers are grouped into actionable segments to optimize marketing spend:

* **Segmentation Logic:** * **VIP:** Customers with  months of history and  in total spend.
* **Regular:** Loyal customers ( months) with spending .
* **New:** Recently acquired customers with a lifespan of  months.


* **KPIs Calculated:** Recency (months since last order), Average Order Value (AOV), and Average Monthly Spend.

### B. Product Performance & Inventory Strategy

A "Part-to-Whole" and performance analysis was conducted to evaluate the product portfolio:

* **Contribution Analysis:** Determining the percentage of total revenue contributed by each category (e.g., how much "Bikes" contribute to the overall  sales).
* **Performance Tiers:** Products are dynamically tagged as **High-Performer** ( revenue), **Mid-Range**, or **Low-Performer**.
* **Profitability:** Comparing average selling price against manufacturing costs to identify margin-rich items.

### C. Advanced Time-Series Analytics

To move beyond basic reporting, the project utilizes complex SQL window functions:

* **Cumulative Sales:** Tracking "Running Totals" to visualize the growth trajectory of the business over time.
* **YoY Analysis:** Using the `LAG()` function to compare a product's current year sales against the previous year to identify growth or decline.
* **Seasonality:** Breaking down sales by `yyyy-MMM` format to pinpoint peak shopping months.

---

## 4. Key Strategic Insights

* **Targeted Loyalty:** The "VIP" segment, though smaller in count, often contributes a disproportionate share of revenue; these should be targeted with exclusive offers.
* **Portfolio Optimization:** By identifying "Low-Performer" products with high costs, the business can decide to discontinue underperforming SKUs.
* **Market Trends:** The "Change Over Time" analysis helps in inventory planning by predicting demand based on historical monthly peaks.

---

## 5. SQL Toolbox (Skills Demonstrated)

* **Window Functions:** `SUM() OVER()`, `AVG() OVER()`, `LAG()`.
* **CTEs (Common Table Expressions):** Used extensively for multi-step data transformations and readability.
* **Conditional Logic:** Complex `CASE` statements for dynamic data segmentation.
* **Date Engineering:** `DATETRUNC`, `DATEDIFF`, and `FORMAT` for time-series intelligence.

<img width="947" height="294" alt="Advanced Analytics" src="https://github.com/user-attachments/assets/a59d4ad8-abcf-4632-8775-88d08cb63d0c" />

