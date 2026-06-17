# chocolate-sales-dashboard
chocolate-sales-dashboard

📊 Project Overview

Objective:
To analyze chocolate sales data and answer three key business questions:

Which regions generate the most revenue and volume?

Which chocolate products perform best in each region?

What are the most popular chocolate types overall?


Tools Used:

Power BI Desktop – Dashboard creation and visualization

Excel – Data cleaning and preparation

GitHub – Version control and portfolio hosting


Key Skills Demonstrated:

Data cleaning and transformation

DAX measure creation

Interactive dashboard design

Business insight generation


📁 Dataset
Source: Chocolate Sales Dataset (Kaggle)

Original Data Structure:

Column	Description
Sales Person	Name of the sales representative
Country	Region of sale
Product	Chocolate product name
Date	Transaction date
Amount	Revenue in USD
Boxes Shipped	Quantity sold

Data Cleaning Steps:

Fixed date format issue (DMY → MDY using Excel Text to Columns)

Removed rows with invalid or missing dates

Verified data types (Date, Decimal, Whole Number, Text)


📈 Dashboard Overview
Page 1: Sales Performance Overview

Visual	Purpose
Total Sales (Revenue)	Card showing $4M total revenue
Total Boxes Shipped	Card showing 100M units
Total Transactions	Card showing 615 orders
Sales by Country	Bar chart showing revenue distribution across regions
Boxes Sold by Product	Bar chart showing volume by product category
Product Performance by Country	Matrix showing revenue breakdown by country and product

Key Insights:

Australia leads in total sales ($4M) and boxes shipped

United Kingdom, India, and USA are the next largest markets

50% Dark Bites is the best-selling product in Australia, India, and USA

Eclairs shows strong performance in India and New Zealand

Business Recommendations:

Focus marketing efforts on top 3 regions (Australia, UK, India)

Promote 50% Dark Bites in underperforming regions to boost sales

Investigate declining product trends in Canada and New Zealand

Bundle top products (50% Dark Bites + Eclairs) for cross-selling opportunities

🛠️ DAX Measures Used
Measure	Formula	Purpose
Total Sales	SUM(Amount)	Total revenue
Total Boxes	SUM(Boxes Shipped)	Total volume sold
Total Transactions	COUNTROWS('Sales')	Number of orders
Sales by Country	SUMMARIZE('Sales', 'Sales'[Country], "Total Sales", SUM('Sales'[Amount]))	Revenue per region
Top Product per Region	TOPN(1, SUMMARIZE(...), [Sales], DESC)	Best product in each country
