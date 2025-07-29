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

## 🧩 Project Pipeline

| Step | Tool | Description |
|------|------|-------------|
| 1️⃣ | **Excel** | Initial Data Understanding, Error Spotting, Null Check, and Pre-cleaning |
| 2️⃣ | **Python (Jupyter)** | Data Cleaning, EDA, KPI Generation, Statistical Analysis (ANOVA, Correlation, Distribution) |
| 3️⃣ | **SQL (MySQL)** | Structured Querying, Joins, Aggregate Calculations, Time-Series Analysis, Data Prep for BI |
| 4️⃣ | **Power BI** | Dashboard Design, Visual Insights, KPI Cards, DAX Measures, Drilldowns, Filters, Page Navigation |

---

## 📊 Project Workflow


---

## 🧩 Step-by-Step Workflow

### 1. 🔍 Excel Data Audit (Initial Exploration)
- Opened `superstore_raw.xlsx` in Excel
- Performed 7 key inspections:
  - Blank/null cells
  - Duplicate rows
  - Irregular formats
  - Spelling/case mismatches
  - Outliers in Profit/Sales
  - Null postal codes
  - Unnecessary columns

> Cleaned version exported as `superstore_cleaned.xlsx`

---

### 2. 🐍 Python – EDA + Statistical Analysis

Scripts:  
- `1_data_cleaning.py`: Data loading, NaN handling, type casting, feature engineering (e.g., profit margin, order month).
- `2_statistical_analysis.py`:  
  - Correlation matrix
  - ANOVA by Region, Segment, and Category
  - Trend charts using Seaborn & Matplotlib

> 📌 **Output**: Statistical patterns on profit margins, segment behavior, seasonal trends.

---

### 3. 🛢️ SQL – Business Querying and Aggregation

Script:  
- `superstore_analysis.sql`

Highlights:
- Data cleaning in SQL (TRIM, CAST, REPLACE)
- Grouped aggregations (Sales, Profit, Quantity)
- Window functions (ROW_NUMBER, RANK)
- Profitability by Segment, State, and Region
- Sales trends by Year, Month, and Category
- High-discount detection

> 📌 **Used for direct connection to Power BI**

---

### 4. 📊 Power BI – Interactive Dashboards

File:  
- `superstore_dashboard.pbix`

Includes:
- 5 professional pages with advanced visuals
  - **Page 1**: Executive Summary (KPIs, Sales/Profit Overview)
  - **Page 2**: Region & State Breakdown (Tree maps, bar charts)
  - **Page 3**: Segment/Product Analysis (Profit Margins, Sales Growth %)
  - **Page 4**: Order Trend Analysis (Line Charts, MoM)
  - **Page 5**: Profitability Deep Dive (Tables, Filters, Slicers)
- DAX Measures used:
  - Total Sales, Total Profit, Profit Margin
  - YoY Growth, Average Order Value, Unique Customers

> Preview:
> ![Dashboard 1](Images/dashboard_preview_1.png)
> ![Dashboard 2](Images/dashboard_preview_2.png)

---

## 📌 Key Insights

- 📈 **Top Regions**: West and East dominate in Sales, but South yields higher margins
- 📦 **High-Performing Categories**: Technology > Office Supplies > Furniture
- 🎯 **High Discounts ≠ High Profit**: Inverse correlation observed
- 🔁 **Repeat Customers**: Key to long-term profitability
- 🛒 **Average Order Value**: Consistent in Q2–Q4 but dips in Q1

---

## 🚀 Future Enhancements

- 📍 Tableau version of dashboards (optional)
- 🔁 Automate cleaning with Python scripts
- 📡 Integrate live SQL connection to Power BI
- 📊 Add forecasting using Power BI + DAX

---

## 📂 File Insertion Guide

| File Type       | Location              | Notes                                  |
|------------------|------------------------|----------------------------------------|
| Excel Raw Data   | `/Data/superstore_raw.xlsx` | Original unprocessed file           |
| Cleaned Excel    | `/Data/superstore_cleaned.xlsx` | Optional after Excel cleaning     |
| Python Scripts   | `/Python/`             | One for cleaning, one for stats        |
| SQL Queries      | `/SQL/superstore_analysis.sql` | All queries in one file           |
| Power BI File    | `/PowerBI/superstore_dashboard.pbix` | Final dashboard                |
| Dashboard Images | `/Images/`             | Screenshots for GitHub README          |

---

## 📧 Contact

If you have any queries or suggestions, feel free to reach out:

**Kranthi Kumar Srimanthula**  
📩 kranthi.ds.project@gmail.com  
📍 Hyderabad, India

---

