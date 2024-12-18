# Walmart Sales Analysis

### Project Overview

This project focuses on analyzing Walmart's sales data to uncover insights about top-performing branches and products, sales trends across various categories, and customer behavior patterns. The objective is to identify opportunities for optimizing sales strategies. The dataset was sourced from the Kaggle Walmart Sales Forecasting Competition.

The competition challenges participants to use historical sales data from 45 Walmart stores across different regions. Each store includes multiple departments, and participants are tasked with forecasting sales for each department. The dataset also includes holiday markdown events, which are known to influence sales, though predicting their impact remains complex.

### Project Objectives
The primary goal of this project is to analyze Walmart's sales data to:

Identify factors influencing sales performance across branches.
Understand customer behavior and product preferences.
Highlight trends and actionable insights to improve sales strategies.
### Dataset Information
The dataset, sourced from the Kaggle Walmart Sales Forecasting Competition, includes sales records from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. It comprises 17 columns and 1,000 rows, providing detailed insights into sales transactions and related factors.
# Tool used
##### Mysql [Download here](https:\\mysql.com)

|Column | Description |Data Type|
|-------|-------------|----------|
|invoice_id |	Invoice of the sales made |	VARCHAR(30)
|branch	|Branch at which sales were made|	VARCHAR(5)
|city	|The location of the branch       | 	VARCHAR(30)
|customer_type |	The type of the customer|	VARCHAR(30)
|gender	|Gender of the customer making purchase |	VARCHAR(10)
|product_line | Product line of the product solf	|VARCHAR(100)
|unit_price |	The price of each product|	DECIMAL(10, 2)
|quantity	|The amount of the product sold|	INT
|VAT	|The amount of tax on the purchase	|FLOAT(6, 4)
|total	|The total cost of the purchase	|DECIMAL(10, 2)
|date	|The date on which the purchase was made|	DATE
|time	|The time at which the purchase was made|	TIMESTAMP
|payment_method|	The total amount paid	|DECIMAL(10, 2)
|cogs|	Cost Of Goods sold|	DECIMAL(10, 2)
|gross_margin_percentage|	Gross margin percentage	|FLOAT(11, 9)
|gross_income|	Gross Income|	DECIMAL(10, 2)
|rating|	Rating|	FLOAT(2, 1)


# Analysis List
### Product Analysis
Conduct analysis on the data to understand the different product lines, the products lines performing best and the product lines that need to be improved.

### Sales Analysis
This analysis aims to answer the question of the sales trends of product. The result of this can help use measure the effectiveness of each sales strategy the business applies and what modificatoins are needed to gain more sales.

### Customer Analysis
This analysis aims to uncover the different customers segments, purchase trends and the profitability of each customer segment.

# Method used

### Data Wrangling:
This is the first step where inspection of data is done to make sure NULL values and missing values are detected and data replacement methods are used to replace, missing or NULL values.

##### Data Inspection: Thoroughly inspected the data to identify and handle missing values (including NULL values).
##### Data Cleaning: Employed appropriate data replacement methods to address missing values.
Data Preparation:

##### Database Creation: Created tables and successfully inserted the data.
# Feature Engineering:
##### Created a time_of_day column to categorize sales into Morning, Afternoon, and Evening, enabling analysis of sales patterns across different parts of the day.
###### Created a day_name column to extract the day of the week (Mon, Tue, Wed, etc.) for each transaction, facilitating analysis of weekly sales trends.
###### Created a month_name column to extract the month of the year (Jan, Feb, Mar, etc.) for each transaction, allowing for analysis of seasonal sales patterns.
# Exploratory Data Analysis (EDA):

Conducted comprehensive EDA to address the defined business questions and achieve the project objectives.
Business Questions to Answer

##### Generic

###### 1 How many unique cities are represented in the data?
###### 2 In which city is each branch located?
# Product

##### How many unique product lines are available?
##### What is the most common payment method used?
##### Which product line has the highest sales volume?
##### What is the total revenue generated each month?
##### In which month were the highest costs of goods sold (COGS) incurred?
##### Which product line generated the highest revenue?
##### Which city generated the highest revenue?
##### Which product line incurred the highest VAT?
##### Classify each product line as "Good" (sales above average) or "Bad" (sales below average).
##### Identify branches that sold more products than the average product sold across all branches.
##### Determine the most common product line purchased by each gender.
##### Calculate the average rating for each product line.
# Sales

##### Analyze the number of sales made during each time of day for each weekday.
##### Identify the customer type that generates the most revenue.
##### Determine the city with the highest tax percentage/VAT.
##### Identify the customer type that pays the highest amount in VAT.
# Customer

##### How many unique customer types are present in the data?
##### How many unique payment methods are used by customers?
##### What is the most common customer type?
##### Which customer type makes the most purchases?
##### Determine the gender distribution among customers.
##### Analyze the gender distribution of customers across different branches.
##### Identify the time of day when customers provide the most ratings.
##### Analyze the time of day when customers provide the most ratings per branch.
##### Determine the day of the week with the highest average customer ratings.
##### Identify the day of the week with the highest average customer ratings per branch.


# Revenue And Profit Calculations
##### $ COGS = unitsPrice * quantity $

##### $ VAT = 5% * COGS $

V
A
T
 is added to the 
C
O
G
S
 and this is what is billed to the customer.

$ total(gross_sales) = VAT + COGS $

$ grossProfit(grossIncome) = total(gross_sales) - COGS $

Gross Margin is gross profit expressed in percentage of the total(gross profit/revenue)

$ \text{Gross Margin} = \frac{\text{gross income}}{\text{total revenue}} $

Example with the first row in our DB:

Data given:

$ \text{Unite Price} = 45.79 $
$ \text{Quantity} = 7 $
$ COGS = 45.79 * 7 = 320.53 $

$ \text{VAT} = 5% * COGS\= 5% 320.53 = 16.0265 $

$ total = VAT + COGS\= 16.0265 + 320.53 = 
336.5565

$ \text{Gross Margin Percentage} = \frac{\text{gross income}}{\text{total revenue}}\=\frac{16.0265}{336.5565} = 0.047619\\approx 4.7619% $


