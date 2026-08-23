Swiggy Revenue Analysis

This project performs an in-depth exploratory data analysis (EDA) and revenue analysis on a dataset of Swiggy food orders. 
The goal is to uncover key performance indicators (KPIs), identify sales trends, understand customer behavior, and pinpoint top-performing entities (cities, restaurants, food types).

Check out the Project :-  https://colab.research.google.com/drive/1OuapFHAMPcjiiXnwGfnQB-UB64arj6nq?usp=sharing

Table of Contents 
Introduction
Dataset
Goals of the Analysis
Methodology
Key Findings and Insights
Dashboard Summary
How to Run the Code
Dependencies
File Structure
Conclusion


Introduction
Swiggy is a prominent online food ordering and delivery platform. Understanding sales patterns, customer preferences, and operational efficiency is crucial for business growth. This analysis leverages a sample Swiggy sales dataset to provide actionable insights into revenue generation, customer satisfaction, and market dynamics.

Dataset
The analysis is based on the swiggy_data.xlsx file, which contains detailed information about individual orders, including:

State, City, Location
Order Date
Restaurant Name
Category, Dish Name
Price (INR)
Rating, Rating Count
Goals of the Analysis
Calculate key business metrics (KPIs) such as total sales, average order value, and average rating.
Identify monthly, daily, quarterly, and weekly sales trends.
Analyze sales distribution across different food types (Veg vs. Non-Veg).
Determine top-performing cities and restaurants by sales volume.
Visualize insights through various charts and a consolidated dashboard.
Methodology


<img width="1706" height="650" alt="image" src="https://github.com/user-attachments/assets/72610e96-c886-4f71-b24e-34183750d317" />


The analysis follows a structured approach:

Data Loading: The swiggy_data.xlsx file is loaded into a Pandas DataFrame.
Initial Data Exploration: Examination of data types, missing values, and summary statistics (df.head(), df.info(), df.describe()).

Data Cleaning and Preparation:
Standardizing column names (e.g., Price (INR) to price_inr).

Converting Order Date to datetime objects.
Creating helper columns: month, quarter, day_of_week, week.

Handling missing Rating and Price values by converting them to numeric and dropping rows with NaN values.
Creating a sales column from price_(inr).

Classifying dishes as 'Veg' or 'Non-Veg' based on keywords in Dish Name.
KPI Calculation:

Total Sales
Average Rating
Total Orders
Average Order Value
Ratings Count


Exploratory Data Analysis (EDA) and Visualization:
Monthly Sales Trend: Line plot showing total sales per month.

Daily Sales Trend: Bar plot showing total sales by day of the week.
Total Sales by Food Type: Bar plot comparing Veg vs. Non-Veg sales.

Total Sales by State (Choropleth Map): Geographic visualization of sales distribution.
Quarterly Performance Summary: Bar plot of total sales per quarter.

Top 5 Cities by Sales: Bar plot of top cities.
Weekly Sales Trend: Line plot showing total sales per week.

Top 5 Restaurants by Sales Volume: List of top restaurants.
Key Findings and Insights

Total Sales & Order Value: The platform generated a Total Sales of ₹53,012,506 with an Average Order Value of ₹218,158, across 243 unique orders.
Customer Satisfaction: The Average Rating stands at 4.34 (out of 5), indicating generally high customer satisfaction with 197,430 ratings recorded.

Sales Trends:
Monthly Sales: Show a consistent performance, with slight fluctuations but no drastic dips or peaks, suggesting stable demand throughout the analyzed months.
Quarterly Sales: Also reflect stability, with Q1 and Q2 showing slightly higher sales compared to Q3, which might indicate seasonal patterns.

Weekly Sales: The weekly trend analysis suggests a steady sales pattern across the weeks, with minor variations.

Daily Sales: Sales are relatively consistent across all days of the week, with a slight peak on weekends (Saturday and Sunday), aligning with typical consumer behavior for food delivery.

Food Type Performance: Vegetarian dishes significantly outperform Non-Vegetarian dishes in terms of total sales, contributing the majority of the revenue.

Top Performing Cities: Bengaluru leads in sales, followed by Lucknow, Hyderabad, Mumbai, and New Delhi, highlighting key geographical markets.
Top Performing Restaurants: Identify the restaurants with the highest sales volume for strategic insights.
Dashboard Summary

All key visualizations and KPIs are consolidated into a single dashboard-style cell, providing a quick and comprehensive overview of Swiggy's sales performance.

<img width="1686" height="670" alt="image" src="https://github.com/user-attachments/assets/f1a90d8c-5f6d-45ca-9f26-ae818936acd3" />


How to Run the Code
Clone the repository:
git clone <repository_url>
cd swiggy-revenue-analysis
Ensure you have the data file: Place swiggy_data.xlsx in the root directory of the project.
Install dependencies (see below).
Open the Jupyter/Colab Notebook: Open swiggy_revenue_analysis.ipynb in your preferred environment (Jupyter Notebook, JupyterLab, Google Colab).
Run all cells: Execute all cells in the notebook sequentially to reproduce the analysis and visualizations.
Dependencies
This project requires the following Python libraries:

pandas
numpy
seaborn
matplotlib
plotly.express
You can install them using pip:

<img width="1722" height="557" alt="image" src="https://github.com/user-attachments/assets/798d85ca-1832-4cd3-b457-0cf3cd3c5eee" />


pip install pandas numpy seaborn matplotlib plotly-express openpyxl
(Note: openpyxl is needed to read .xlsx files with pandas)

File Structure
swiggy-revenue-analysis/

├── swiggy_data.xlsx         # Input dataset

├── swiggy_revenue_analysis.ipynb # Jupyter/Colab Notebook with the analysis

├── swiggy_processed_data.csv # Output: Processed data after cleaning

└── swiggy_sales_dashboard.png # Output: Image of the consolidated dashboard


# 🍔 Swiggy Sales Analysis Dashboard | Advanced Excel | WPS 

## 📊 Project Overview

This project presents an **interactive Swiggy Sales Analysis Dashboard** developed using **Advanced Excel techniques** to analyze sales, orders, ratings, customer activity, and geographic performance.

The dashboard transforms raw restaurant and food-order data into meaningful business insights through **PivotTables, PivotCharts, KPI cards, calculated fields, filters, and interactive dashboard components**.

The objective of this project is to demonstrate how an analyst can transform a large raw dataset into a **management-ready business dashboard** that supports quick and data-driven decision-making.

---

## 🎯 Business Objective

The primary objective is to analyze Swiggy-style food-order data and answer important business questions such as:

* How much total revenue was generated?
* How many orders were recorded?
* What is the average customer rating?
* Which months generated the highest sales?
* Which cities contribute the most revenue?
* Which states have the highest sales?
* Which days of the week generate higher sales?
* How does quarterly performance change?
* Which food categories contribute most to sales?
* How many customer ratings were recorded?

---

## 🗂️ Dataset

The dataset contains approximately **50,000+ records** and includes restaurant and food-order information.

### Key Fields

| Field           | Description                                 |
| --------------- | ------------------------------------------- |
| State           | State where the restaurant/order is located |
| City            | City associated with the restaurant/order   |
| Order Date      | Date of the order                           |
| Restaurant Name | Restaurant associated with the order        |
| Location        | Restaurant/location information             |
| Category        | Food/category classification                |
| Dish Name       | Name of the food item                       |
| Price           | Price/value used for sales analysis         |
| Rating          | Customer rating                             |
| Rating Count    | Number of ratings associated with the item  |

---

## 🛠️ Tools & Techniques Used

### Tools

* **Microsoft Excel concepts**
* **WPS Spreadsheet** for implementation
* Advanced Excel / Spreadsheet techniques

### Techniques

* Data Cleaning & Preparation
* Excel Tables
* PivotTables
* PivotCharts
* KPI Cards
* Calculated Fields
* Helper Columns
* Date & Time Analysis
* Sales Aggregation
* Sorting & Ranking
* Interactive Filters
* Dashboard Design
* Conditional Formatting
* Business KPI Analysis

---

# 📌 Dashboard KPIs

The dashboard focuses on four major performance indicators:

### 💰 Total Sales

Measures the overall sales value generated from the dataset.

### ⭐ Average Rating

Measures the average customer rating across the available records.

### 📦 Total Orders

Represents the number of records/orders used for the analysis based on the dataset structure.

### 👥 Rating Count

Represents the aggregated rating activity available in the dataset.

---  <img width="1553" height="585" alt="image" src="https://github.com/user-attachments/assets/833702ac-85aa-4e14-bb35-78ce06f64003" />


# 📈 Dashboard Analysis

## 1. Monthly Sales Trend

A line chart is used to analyze how sales change throughout the months.

**Business Question:**

> Which months demonstrate stronger or weaker sales performance?

This can help identify seasonal patterns and changes in monthly demand.

---   <img width="1853" height="708" alt="image" src="https://github.com/user-attachments/assets/86649af4-17cf-4aeb-a32a-5e2b5ad0616c" />


## 2. Weekly Sales Trend

Sales are analyzed across different weekdays to identify high-performing and low-performing days.

**Business Question:**

> Which days of the week generate the highest sales?

This can support operational planning and promotional decisions.

---   <img width="1890" height="724" alt="image" src="https://github.com/user-attachments/assets/7b33c80a-ea7a-4fc9-8738-0c0bb6116e5d" />


## 3. Top 5 Cities by Sales

The dashboard ranks cities based on total sales.

**Business Question:**

> Which cities contribute the most to overall sales?

This helps identify high-value markets.

---  <img width="1879" height="577" alt="image" src="https://github.com/user-attachments/assets/3051caa2-520b-4c78-9bec-d8d757ec1277" />


## 4. Top 5 States by Sales

A state-level comparison highlights the strongest geographical markets.

**Business Question:**

> Which states generate the highest sales?

This provides a broader view of regional business performance.

---  <img width="885" height="516" alt="image" src="https://github.com/user-attachments/assets/9ed1bb46-5ff5-4cb5-acac-51e04ae7cc87" />


## 5. Sales by Food Category

The dashboard analyzes sales contribution across food categories.

**Business Question:**

> Which food categories contribute most to sales?

This can help identify popular product segments.

---   <img width="1041" height="422" alt="image" src="https://github.com/user-attachments/assets/ce4fb4c6-4ada-4f36-a244-65be5fcda062" />


## 6. Quarterly Performance

Sales performance is compared across quarters.

The analysis can be used to evaluate:

* Sales
* Order volume
* Average rating

**Business Question:**

> Which quarter demonstrates the strongest overall performance?

--- <img width="1634" height="528" alt="image" src="https://github.com/user-attachments/assets/578ab9c5-6e19-4b2a-8e3e-047d338ef3ed" />


# 🎛️ Interactive Dashboard

The dashboard includes interactive filtering functionality for fields such as:

* State
* Month
* Quarter

These filters are intended to allow users to explore the dashboard from different business perspectives.

---

# 🧮 Helper Columns

Additional date-based fields were created to support time-series analysis, including:

* Month
* Month Number
* Quarter
* Week Number
* Weekday
* Year

These fields make it easier to group and analyze sales performance through PivotTables and PivotCharts.

---

# 🔍 Key Business Insights

The dashboard allows stakeholders to quickly identify:

* Overall sales performance
* Monthly sales movement
* High-performing cities
* High-performing states
* Weekly sales patterns
* Quarterly performance
* Food-category contribution
* Customer rating activity

The dashboard is designed to convert raw transactional data into **actionable business information** rather than presenting raw numbers alone.

---

# 📊 Dashboard Preview

> Add your final dashboard screenshot here.

```text
![Swiggy Sales Analysis Dashboard](Dashboard.png)
```

For GitHub, save your screenshot as:

`Dashboard.png`

and place it in the same repository folder as this README.

---

# 📁 Repository Structure

```text
Swiggy-Sales-Analysis-Dashboard/
│
├── 📊 Swiggy_Sales_Dashboard.xlsx
├── 🖼️ Dashboard.png
├── 📄 BRD.pdf
├── 📄 README.md
└── 📂 Dataset/
    └── Swiggy_Sales_Data.xlsx
```

If you don't want to upload the complete dataset because of file size or data-sharing restrictions, you can omit the dataset folder and provide a short description of the dataset instead.

---

# 💡 Skills Demonstrated

This project demonstrates practical experience in:

* Advanced Excel
* Data Analysis
* Business Intelligence
* Dashboard Development
* Data Visualization
* PivotTables
* PivotCharts
* KPI Development
* Time-Series Analysis
* Geographic Analysis
* Business Reporting
* Data Storytelling

---

# 🚀 Future Improvements

Potential improvements for the next version include:

* Power BI implementation
* Automated data refresh
* Dynamic KPI comparisons
* Year-over-Year growth analysis
* Profit and margin analysis if cost data becomes available
* Customer segmentation
* Restaurant-level performance analysis
* Advanced Power Query transformation
* Automated dashboard refresh

---

# 👨‍💻 Author

**Arya Marale**

BCA Graduate | Data Analyst Aspirant

### Technical Skills

`Excel` • `Power BI` • `SQL` • `Python` • `Data Visualization` • `Machine Learning`

---

## ⭐ Project Purpose

This project was created as part of my **Data Analyst portfolio** to demonstrate practical ability in transforming raw business data into an interactive and management-friendly dashboard.

The focus is not only on creating charts, but on understanding the **business questions behind the data and presenting insights in a clear, decision-oriented format**.

---

### 📌 Project Status

**Completed ✅**

**Dashboard:** Advanced Excel / WPS Spreadsheet
**Analysis:** Sales, Orders, Ratings & Geographic Performance
**Data:** Restaurant/Food Order Dataset


Conclusion
This analysis provides a foundational understanding of Swiggy's sales performance. The insights gained can be valuable for strategic decision-making, such as optimizing marketing campaigns, identifying growth opportunities in specific cities, and tailoring menu offerings based on food type preferences. Further analysis could delve into customer segmentation, delivery efficiency, and pricing strategies.
