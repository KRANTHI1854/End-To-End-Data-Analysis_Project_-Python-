# 📊 Superstore Sales Analysis Project

## 🧾 Project Title: End-to-End Sales & Operations Analytics Using Excel, SQL, Python & Power BI

---

## 📁 Project Overview

This project focuses on analyzing the performance of a retail Superstore using an end-to-end data analytics approach. I have applied **Excel, SQL, Python, and Power BI** to clean, transform, analyze, and visualize the data. The goal is to deliver key business insights that support decision-making for areas such as sales growth, regional performance, customer behavior, shipping efficiency, and product profitability.

---

## 🔧 Tools & Technologies Used

| Tool         | Purpose                                      |
|--------------|----------------------------------------------|
| Excel        | Initial data inspection and cleaning         |
| MySQL        | Advanced data transformation and querying    |
| Python (Pandas, Matplotlib, Seaborn) | EDA, KPIs, statistics, and visual storytelling |
| Power BI     | Interactive dashboard creation using DAX     |

---

## 📊 Project Workflow

### ✅ Phase 1: Data Understanding & Cleaning (Excel)
- Removed duplicates, blanks, and inconsistent data types
- Standardized date and text formats
- Validated business columns like Sales, Profit, Discount

### ✅ Phase 2: Data Analysis & Visualization (Python)
- Cleaned data using **Pandas**
- Generated KPIs such as:
  - Total Sales, Profit, Orders
  - Average Profit Margin
  - Top/Bottom Products by Profit
- Visualized trends using:
  - Line charts (sales over time)
  - Bar charts (region/category-wise sales)
  - Donut and Pie charts (shipping & customer segments)
- Used statistical measures for correlation and outliers

### ✅ Phase 3: Structured Query Language (SQL - MySQL)
- Wrote 40+ professional queries covering:
  - Profitability by segment, region, and category
  - Yearly and monthly trends
  - Late deliveries and impact on customer satisfaction
  - Repeat vs new customers
  - Profit/loss identification using advanced SQL (CTEs, window functions)

### ✅ Phase 4: Interactive Dashboard (Power BI)
- Designed a 7-page dashboard with the following sections:
  1. **Executive Summary**
  2. **Region-wise Sales & Profit**
  3. **Customer Behavior Analysis**
  4. **Shipping & Delivery Trends**
  5. **Time Series Performance**
  6. **Advanced Business KPIs**
  7. **Product Performance Deep Dive**
- Built using **DAX measures** for dynamic KPIs
- Slicers and filters enabled for interactivity (Year, Segment, Region, etc.)
- Custom visualizations like:
  - Funnel Chart (Shipping stages)
  - Matrix Table (Profit by Sub-Category & Region)
  - Heatmaps (Late delivery concentration by State)

---

## 💼 Business Goals Addressed

- 📈 Improve regional profitability and discover underperforming areas
- 🚚 Optimize shipping timelines and detect frequent delays
- 🛍️ Understand customer segmentation and repeat behavior
- 🧮 Identify product lines with high margins or frequent losses
- 🕒 Analyze sales & order trends over time for seasonal planning

---

## 📁 File Structure

```plaintext
📂 Superstore-Analytics-Project/
│
├── 📄 README.md                 # This file
├── 📊 super_store_analysis.pbix # Power BI dashboard (7 pages)
├── 📈 cleaned_superstore_data.csv # Final cleaned dataset
├── 🐍 superstore_analysis.py    # Python EDA & visualizations
├── 📑 superstore_queries.sql    # SQL queries and views
├── 📊 images/                   # Exported Power BI visuals (optional)
