Swiggy Revenue Analysis

This project performs an in-depth exploratory data analysis (EDA) and revenue analysis on a dataset of Swiggy food orders. 
The goal is to uncover key performance indicators (KPIs), identify sales trends, understand customer behavior, and pinpoint top-performing entities (cities, restaurants, food types).

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

pip install pandas numpy seaborn matplotlib plotly-express openpyxl
(Note: openpyxl is needed to read .xlsx files with pandas)

File Structure
swiggy-revenue-analysis/
├── swiggy_data.xlsx         # Input dataset
├── swiggy_revenue_analysis.ipynb # Jupyter/Colab Notebook with the analysis
├── swiggy_processed_data.csv # Output: Processed data after cleaning
└── swiggy_sales_dashboard.png # Output: Image of the consolidated dashboard
Conclusion
This analysis provides a foundational understanding of Swiggy's sales performance. The insights gained can be valuable for strategic decision-making, such as optimizing marketing campaigns, identifying growth opportunities in specific cities, and tailoring menu offerings based on food type preferences. Further analysis could delve into customer segmentation, delivery efficiency, and pricing strategies.
