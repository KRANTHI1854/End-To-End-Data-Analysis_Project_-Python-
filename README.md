# 📊 Superstore Sales Analysis Project

## 🧾 Project Title: End-to-End Sales & Operations Analytics Using Excel, SQL, Python & Power BI

---

This project focuses on analyzing the performance of a retail Superstore using an end-to-end data analytics approach. I have applied **Excel, SQL, Python, and Power BI** to clean, transform, analyze, and visualize the data. The goal is to deliver key business insights that support decision-making for areas such as sales growth, regional performance, customer behavior, shipping efficiency, and product profitability.

---

## 🧩 Project Pipeline

| Step | Tool | Description |
|------|------|-------------|
| 1️⃣ | **Excel** | Initial Data Understanding, Error Spotting, Null Check, and Pre-cleaning |
| 2️⃣ | **Python (Jupyter)** | Data Cleaning, ETL, EDA, KPI Generation, Statistical Analysis (ANOVA, Correlation, Distribution) |
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

> Cleaned version exported as `cleaned superstore data.csv`
 #### 📁 Raw Dataset : 
<a href="https://github.com/KRANTHI1854/End-To-End-Data-Analysis_Project_-Python-/blob/main/supper%20store%20data%20set.csv">supper store data set.csv</a>

#### 📁 Cleaned Dataset : 
<a href="https://github.com/KRANTHI1854/End-To-End-Data-Analysis_Project_-Python-/blob/main/cleaned_superstore_data.csv">cleaned_superstore_data.csv</a>


---

### 2. 🐍 Python – ETL + EDA + Statistical Analysis

---

#### 🔸 1_data_cleaning.py – ETL & Feature Engineering

**Purpose**: Clean and prepare the dataset for analysis.

**Steps Performed**:
- 📥 **Data Import**  
  `pd.read_excel()` used to load the raw dataset.

- 🧼 **Missing Value Handling**  
  Identified missing values using `.isnull().sum()`  
  Handled via `dropna()` or appropriate imputation.

- 🧪 **Data Type Casting**  
  Converted columns like `order_date`, `ship_date` to `datetime`.

- 🏷 **Column Renaming**  
  Renamed columns to `snake_case` format for readability.

- 🛠 **Feature Engineering**:
  - `profit_margin = profit / sales`
  - `order_month`, `order_year` from `order_date`
  - `delivery_days = ship_date - order_date`
  - `customer_repeat_flag` to identify returning customers

- ✅ **Output File**:  
  Cleaned dataset saved as `superstore_cleaned.xlsx`  
  Ready for SQL upload and Power BI/Tableau integration.

---

#### 🔸 2_statistical_analysis.py – EDA + Statistical Modelling

**Purpose**: Uncover hidden patterns in data using EDA & hypothesis testing.

**Libraries Used**:
- `pandas`, `numpy` – data handling  
- `seaborn`, `matplotlib.pyplot` – data visualization  
- `scipy.stats` – ANOVA, statistical tests  
- `statsmodels` (optional) – regression analysis

**Analysis Performed**:

- 📊 **Descriptive Statistics**  
  Used `.describe()`, `.value_counts()` to understand distribution.

- 🔗 **Correlation Matrix**  
  - `df.corr()` to examine relationships  
  - Visualized using `seaborn.heatmap()`

- 🧪 **ANOVA Tests**:
  - `f_oneway()` used for comparing means of:
    - `Region` → Are profits significantly different?
    - `Segment` → How do customer types differ?
    - `Category` → Which categories perform better?

- 📈 **Trend & Pattern Analysis**:
  - Monthly sales/profit using `lineplot()`
  - Segment-wise trends
  - Discount vs. profit margin (scatterplot)

- 📌 **Insights Delivered**:
  - Key drivers of profit margin
  - Statistically significant segment/category/region behaviors
  - Seasonal performance trends
####📁 Python file:
     [🐍 Python Analysis Code](https://github.com/KRANTHI1854/End-To-End-Data-Analysis_Project_-Python-/blob/main/superstore_data_insights.ipynb)

---

### 3. 🛢️ SQL – Business Querying and Aggregation

---

#### 🎯 Objective:
Perform professional-grade business analysis directly in SQL to extract insights, perform aggregation, apply logic, and prepare data for dashboarding (Power BI).

---

#### 📊 Aggregation & Business Metrics:
- **Grouped Aggregations**:
  - Total `Sales`, `Profit`, and `Quantity` grouped by:
    - `Region`, `State`, `Segment`, `Category`, and `Order_Year`
  - Used `GROUP BY` with `ORDER BY` for logical insights.

- **Profitability Analysis**:
  - Calculated `Profit Margin = profit / sales`
  - Identified top-performing `Segment`, `State`, and `Region` based on margin.

- **Trend Analysis**:
  - Yearly and Monthly Sales trends using:
    ```sql
    EXTRACT(YEAR FROM order_date) AS order_year,
    EXTRACT(MONTH FROM order_date) AS order_month
    ```
  - Sales growth trend for `Category`, `Sub-Category`.

---

#### 🪟 Window Functions:
- Applied powerful **analytical window functions** for ranking and tracking:
  - `ROW_NUMBER()` – Unique row identification for deduplication
  - `RANK()` – Ranking states by sales or profit
  - `DENSE_RANK()` – To identify top categories across years

---

#### 🚨 High Discount Detection:
- Flagged orders where:
  ```sql
  discount > 0.3
####🛢️Sql File: 
[SQL Business Queries](https://github.com/KRANTHI1854/End-To-End-Data-Analysis_Project_-Python-/blob/main/sql%20codes)

---

### 4. 📊 Power BI – Interactive Dashboards

---

#### 📌 Overview:
This Power BI dashboard delivers **actionable business insights** across 5 professional-grade report pages. Each page leverages **real-time SQL connection**, dynamic filters, and DAX measures for performance evaluation and decision support.

---

#### 📄 Dashboard Pages & Visual Highlights:

---

🔹 **Page 1 – Executive Summary**  
> ✴️ KPIs | Sales, Profit, Orders  
> 📈 Donut Chart – Sales Share by Segment  
> 📊 Bar Chart – YoY Sales Comparison  
> 🎯 KPI Cards – Total Sales, Profit, Quantity, Orders  

---

🔹 **Page 2 – Regional & State-wise Breakdown**  
> 🌍 Tree Map – Total Sales by Region  
> 🗺️ Bar Chart – State-wise Profit  
> 📌 Slicer – Filter by Region  
> 🧭 Table – Region vs Profit Margin  

---

🔹 **Page 3 – Segment/Product Insights**  
> 🧩 Clustered Bar Chart – Segment-wise Sales Growth %  
> 💡 Profit Margin Analysis – Category vs Sub-Category  
> 🔄 YoY Trend – Sales by Segment  
> 🎛️ Slicer – Category Selector  

---

🔹 **Page 4 – Order Trend Analysis**  
> 📅 Line Charts – Month-over-Month Sales & Orders  
> 🕐 Timeline View – Monthly Trends by Year  
> 📌 Area Chart – Category Sales Trend  
> 📆 Year & Month Slicers  

---

🔹 **Page 5 – Profitability Deep Dive**  
> 🧾 Table – Product-wise Profit Margin  
> 🎯 Filters – State, Segment, Category  
> 📊 KPI Cards – Avg. Order Value, Total Discount, Unique Customers  
> 📌 Matrix – Profit Contribution by Product Line  

---

#### 🧮 DAX Measures Used:

##### 🛍️ Sales Metrics:
- `Total Sales = SUM('superstore cleaned_superstore_data'[Sales])`
- `Average Sales = AVERAGE('superstore cleaned_superstore_data'[Sales])`
- `Total Orders = DISTINCTCOUNT('superstore cleaned_superstore_data'[Order ID])`
- `Sales Growth (%) = DIVIDE([Current Sales] - [Previous Sales], [Previous Sales])`

##### 💰 Profitability Metrics:
- `Total Profit = SUM('superstore cleaned_superstore_data'[Profit])`
- `Profit Margin = DIVIDE([Total Profit], [Total Sales])`
- `Total Discount = SUM('superstore cleaned_superstore_data'[Discount])`
- `Avg. Discount = AVERAGE('superstore cleaned_superstore_data'[Discount])`

##### 👥 Customer Analysis:
- `Unique Customers = DISTINCTCOUNT('superstore cleaned_superstore_data'[Customer ID])`
- `Average Order Value = DIVIDE([Total Sales], [Total Orders])`
- `Repeat Purchase Rate = DIVIDE(COUNTROWS(FILTER('superstore cleaned_superstore_data', [Repeat Customer Flag] = TRUE)), [Unique Customers])`  
  *(if applied)*

##### 📈 Trend Analysis:
- `YoY Sales = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('superstore cleaned_superstore_data'[Order Date]))`
- `MoM Sales = CALCULATE([Total Sales], PARALLELPERIOD('superstore cleaned_superstore_data'[Order Date], -1, MONTH))`
- `YoY Sales Growth = DIVIDE([Total Sales] - [YoY Sales], [YoY Sales])`
- `Monthly Sales Trend = TOTALYTD([Total Sales], 'superstore cleaned_superstore_data'[Order Date])`

##### 📦 Product/Segment Breakdown:
- `Sales by Segment = CALCULATE([Total Sales], ALLEXCEPT('superstore cleaned_superstore_data', 'superstore cleaned_superstore_data'[Segment]))`
- `Profit by Category = CALCULATE([Total Profit], ALLEXCEPT('superstore cleaned_superstore_data', 'superstore cleaned_superstore_data'[Category]))`
- `Top Selling Product = RANKX(ALL('superstore cleaned_superstore_data'[Product Name]), [Total Sales], , DESC)`

##### 📌 Other Key Measures:
- `Order Quantity = SUM('superstore cleaned_superstore_data'[Quantity])`
- `Total Products Sold = DISTINCTCOUNT('superstore cleaned_superstore_data'[Product ID])`
- `High Discount Orders = CALCULATE(COUNTROWS('superstore cleaned_superstore_data'), 'superstore cleaned_superstore_data'[Discount] > 0.2)`
- `Late Orders Count = CALCULATE(COUNTROWS('superstore cleaned_superstore_data'), 'superstore cleaned_superstore_data'[Ship Date] > 'superstore cleaned_superstore_data'[Order Date] + 3)`

---

#### 🧩 Visual Types Used:
- KPI Cards, Line Charts, Bar Charts, Tree Maps, Area Charts, Donuts, Matrix Table, Slicers, Filters

---

#### 🔌 SQL + Power BI Integration:
- Direct SQL connection using `superstore_analysis.sql` file
- Dynamic SQL queries ensure real-time sync with dashboards
- Avoided SQL Views to maintain drag-and-drop flexibility in visuals

## 📌 Key Insights

- 📈 **Top Regions**: West and East dominate in Sales, but South yields higher margins
- 📦 **High-Performing Categories**: Technology > Office Supplies > Furniture
- 🎯 **High Discounts ≠ High Profit**: Inverse correlation observed
- 🔁 **Repeat Customers**: Key to long-term profitability
- 🛒 **Average Order Value**: Consistent in Q2–Q4 but dips in Q1

#### POWER BI File 📁: 
[Power BI Dashboard File](https://github.com/KRANTHI1854/End-To-End-Data-Analysis_Project_-Python-/blob/main/super_store_analysis.pbix)

---



