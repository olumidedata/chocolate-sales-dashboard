# chocolate-sales-dashboard
chocolate-sales-dashboard

📊 Project Overview

Objective:
To analyze chocolate sales data and answer three key business questions:

1. Which regions generate the most revenue and volume?

2. Which chocolate products perform best in each region?

3. What are the most popular chocolate types overall?


Tools Used:

1. Power BI Desktop – Dashboard creation and visualization

2. Excel – Data cleaning and preparation

3. GitHub – Version control and portfolio hosting


Key Skills Demonstrated:

1. Data cleaning and transformation

2. DAX measure creation

3. nteractive dashboard design
   

Business insight generation

📁 Dataset
Source: Chocolate Sales Dataset (Kaggle)

Original Data Structure:

Column	Description

1. Sales Person -	Name of the sales representative
2. Country	- Region of sale
3. Product	- Chocolate product name
4. Date -	Transaction date
5. Amount -	Revenue in USD
6. Boxes Shipped	- Quantity sold

Data Cleaning Steps:

1. Fixed date format issue (DMY → MDY using Excel Text to Columns)

2. Removed rows with invalid or missing dates

3. Verified data types (Date, Decimal, Whole Number, Text)


📈 Dashboard Overview
Page 1: Sales Performance Overview

Visual	Purpose

1. Total Sales (Revenue)	Card - showing $4M total revenue
2. Total Boxes Shipped	Card - showing 100M units
3. Total Transactions	Card - showing 615 orders
4. Sales by Country	Bar chart - showing revenue distribution across regions
5. Boxes Sold by Product	Bar chart - showing volume by product category
6. Product Performance by Country	Matrix - showing revenue breakdown by country and product

Key Insights:

1. Australia leads in total sales ($4M) and boxes shipped

2. United Kingdom, India, and USA are the next largest markets

3. 50% Dark Bites is the best-selling product in Australia, India, and USA

3. Eclairs shows strong performance in India and New Zealand

Business Recommendations:

1. Focus marketing efforts on top 3 regions (Australia, UK, India)

2. Promote 50% Dark Bites in underperforming regions to boost sales

3. Investigate declining product trends in Canada and New Zealand

4. Bundle top products (50% Dark Bites + Eclairs) for cross-selling opportunities

🛠️ DAX Measures Used

Measure	Formula	Purpose

Total Sales	SUM(Amount)	Total revenue
Total Boxes	SUM(Boxes Shipped)	Total volume sold
Total Transactions	COUNTROWS('Sales')	Number of orders
Sales by Country	SUMMARIZE('Sales', 'Sales'[Country], "Total Sales", SUM('Sales'[Amount]))	Revenue per region
Top Product per Region	TOPN(1, SUMMARIZE(...), [Sales], DESC)	Best product in each country
