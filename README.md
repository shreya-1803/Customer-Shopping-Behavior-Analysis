# 🛒 Customer Shopping Behavior Analysis

An end-to-end Data Analytics & Business Intelligence project designed to evaluate customer purchasing patterns, discount effectiveness, subscription dynamics, and demographic segmentations using **SQL (MySQL)**, **Python**, and **Power BI**.

---

## 📌 Project Overview

In today's competitive retail landscape, transforming raw transactional data into actionable business intelligence is essential for optimizing revenue and driving customer retention. This project processes and analyzes customer transaction datasets to answer core business questions around spending behavior, customer loyalty, product popularity, and promotional strategy impact.

The analytical pipeline spans initial data cleaning and feature engineering in **Python**, multi-dimensional SQL querying in **MySQL**, exploratory data analysis (EDA) using **Matplotlib & Seaborn**, and the deployment of an interactive executive dashboard in **Power BI**.

---

## 🎯 Objectives

- **Demographic Analysis:** Evaluate customer spending habits across age groups and gender distributions.
- **Promotional Impact:** Measure the financial effectiveness of discounts and sales promotions on total revenue.
- **Subscription Dynamics:** Compare purchasing frequency, average order value (AOV), and retention metrics between subscribers and non-subscribers.
- **Customer Segmentation:** Classify customers into actionable tiers (*New*, *Returning*, *Loyal*) based on historical purchase frequency.
- **Product Performance:** Identify top-performing product categories and inventory items driving overall top-line growth.
- **Interactive BI Dashboard:** Build an interactive Power BI dashboard with dynamic slicers and KPIs for strategic decision-making.

---

## 🛠️ Tech Stack & Tools

| Category | Tool / Library | Key Use Case / Purpose |
| :--- | :--- | :--- |
| **Database Management** | MySQL | Data querying, aggregations, conditional joins, and segment filtering |
| **Data Processing** | Python (Pandas) | Data cleaning, missing value handling, type conversion, feature engineering |
| **Numeric Computations** | Python (NumPy) | Statistical calculation, mathematical logic, and array manipulation |
| **Exploratory Visualization** | Matplotlib & Seaborn | Trend charts, histograms, heatmaps, distribution plots, and boxplots |
| **Business Intelligence** | Power BI | Interactive dashboard development, KPI tracking, and drill-down filters |

---

## 📂 Dataset Overview

The project relies on customer transactional records containing key demographic, financial, and behavioral attributes:

- **Customer Demographics:** `Age`, `Gender`
- **Transaction Details:** `Product Category`, `Item Purchased`, `Purchase Amount ($)`
- **Behavioral Attributes:** `Discount Applied` (Yes/No), `Subscription Status` (Yes/No)
- **Customer Lifecycle Data:** `Previous Purchases` (Transaction Frequency)

---

## ⚙️ Project Methodology Pipeline

1. **Data Ingestion & Inspection:** Loading raw dataset, auditing schema types, missing values, and null record distribution.
2. **Data Cleaning & Feature Engineering (Pandas):**
   - Handling missing/null records.
   - Standardizing numerical formatting and categorical labels.
   - Deriving calculated columns: `Age Group` bins, `Customer Segment` tags (*New*, *Returning*, *Loyal*).
3. **Relational Database Analysis (MySQL):**
   - Importing cleaned data into MySQL.
   - Running analytical SQL queries utilizing `GROUP BY`, aggregate functions (`SUM`, `AVG`, `COUNT`), window functions, and `CASE` conditional logic.
4. **Exploratory Data Analysis (Python Visualization):**
   - Uncovering correlations between age and spend using Seaborn heatmaps.
   - Examining purchase distribution across product categories via Seaborn/Matplotlib bar and distribution plots.
5. **Dashboard Development & Reporting (Power BI):**
   - Designing dynamic visuals, executive KPIs (Total Revenue, Average Order Value, Total Customers).
   - Implementing interactive slicers for Category, Gender, Subscription Status, and Age Group filterability.

---

## 📊 Key Insights & Analysis Areas

- **Revenue Breakdown:** Comparative revenue contribution by age bracket and gender identification.
- **Discount vs. Full Price:** Revenue yield analysis evaluating whether discount promotions increase order volume without diluting margin.
- **Subscriber Value:** Comparative assessment showing higher overall lifetime spend and retention among subscribed members.
- **Customer Lifetime Segments:**
  - **New:** 1st purchase customers.
  - **Returning:** 2 to 5 prior purchases.
  - **Loyal:** 6+ prior purchases.
- **Top Product Categories:** Product category benchmarking to optimize marketing spend and stock allocation.

---

## 📁 Repository Structure

```text
├── data/
│   ├── raw_customer_data.csv       # Raw input transaction dataset
│   └── cleaned_customer_data.csv   # Processed dataset ready for SQL/Power BI
├── sql/
│   ├── schema.sql                  # Database creation and table definition
│   └── analysis_queries.sql        # Business queries and aggregation logic
├── notebooks/
│   ├── 01_data_cleaning.ipynb      # Pandas cleaning & feature engineering script
│   └── 02_exploratory_analysis.ipynb # Seaborn/Matplotlib visualization code
├── dashboards/
│   └── customer_behavior_dashboard.pbix # Power BI interactive dashboard file
├── README.md                       # Documentation
└── requirements.txt                # Python environment dependencies
