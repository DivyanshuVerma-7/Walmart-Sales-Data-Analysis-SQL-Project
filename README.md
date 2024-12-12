# Walmart-Sales-Data-Analysis-SQL-Project
## ![walmart](https://github.com/user-attachments/assets/f81e25bc-7249-48d4-ab43-db660157d195)  
## About  
This project involves analyzing Walmart's sales data to identify top-performing branches and products, uncover sales patterns, and gain insights into customer behavior. The primary aim is to optimize and enhance sales strategies. The dataset used for this analysis comes from the [Kaggle Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting).
## Project Objectives  
The primary goal is to derive insights from Walmart's sales data, examining various factors that impact sales across different branches.  
## Data Overview  
The dataset, sourced from the Kaggle Walmart Sales Forecasting Competition, includes sales records from three Walmart branches located in Mandalay, Yangon, and Naypyitaw. It comprises 17 columns and 1,000 rows.
## Data Dictionary

| Column              | Description                        | Data Type       |
|---------------------|------------------------------------|-----------------|
| `invoice_id`        | Invoice of the sales made          | `VARCHAR(30)`   |
| `branch`            | Branch at which sales were made    | `VARCHAR(5)`    |
| `city`              | The location of the branch         | `VARCHAR(30)`   |
| `customer_type`     | The type of the customer           | `VARCHAR(30)`   |
| `gender`            | Gender of the customer making a purchase | `VARCHAR(10)`   |
| `product_line`      | Product line of the product sold   | `VARCHAR(100)`  |
| `unit_price`        | The price of each product          | `DECIMAL(10, 2)`|
| `quantity`          | The amount of the product sold     | `INT`           |
| `VAT`               | The amount of tax on the purchase  | `FLOAT(6, 4)`   |
| `total`             | The total cost of the purchase     | `DECIMAL(12, 4)`|
| `date`              | The date on which the purchase was made | `DATETIME` |
| `time`              | The time at which the purchase was made | `TIME`      |
| `payment`           | The total amount paid              | `DECIMAL(10, 2)`|
| `cogs`              | Cost Of Goods Sold                 | `DECIMAL(10, 2)`|
| `gross_margin_pct`  | Gross margin percentage            | `FLOAT(11, 9)`  |
| `gross_income`      | Gross Income                       | `DECIMAL(12, 4)`|
| `rating`            | Rating                             | `FLOAT(2, 1)`   |

## Analysis Categories
### Product Analysis
Analyze the data to uncover insights about different product lines, identify the top-performing ones, and pinpoint areas where other product lines could improve.

### Sales Analysis
This analysis aims to explore sales trends across products. The findings will help assess the effectiveness of existing sales strategies and identify areas for improvement to boost overall sales.

### Customer Analysis
Focus on segmenting customers, understanding their purchasing behaviors, and evaluating the profitability of each customer segment.
## Approach
### 1. Data Wrangling

In this initial step, the dataset is reviewed for NULL or missing values, and appropriate strategies are applied to handle and replace them.
* Building a Database.
* Create a database table and insert the data.
* Check for columns with NULL values. In this case, no NULL values were present because the NOT NULL constraint was applied during table creation.
### 2. Feature Engineering
Generate new features to derive additional insights:
* time_of_day: Categorize sales into Morning, Afternoon, and Evening to determine which part of the day sees the highest sales.
* day_name: Extract the day of the week (e.g., Mon, Tue) for each transaction to identify the busiest days for each branch.
* month_name: Extract the month (e.g., Jan, Feb) to determine which month generates the most sales and profit.
### 3. Exploratory Data Analysis (EDA)

Perform EDA to answer key questions and meet the objectives of the project.

## Business Questions to Answer
### Generic Questions  
1. How many distinct cities are present in the dataset?
2. In which city is each branch situated?
### Product Analysis
1. How many distinct product lines are there in the dataset?
2. What is the most common payment method?
3. What is the most selling product line?
4. What is the total revenue by month?
5. Which month recorded the highest Cost of Goods Sold (COGS)?
6. Which product line generated the highest revenue?
7. Which city has the highest revenue?
8. Which product line incurred the highest VAT?
9. Retrieve each product line and add a column product_category, indicating 'Good' or 'Bad,' based on whether its sales are above the average.
10. Which branch sold more products than average product sold?
11. What is the most common product line by gender?
12. What is the average rating of each product line?
### Sales Analysis
1. Number of sales made in each time of the day per weekday
2. Identify the customer type that generates the highest revenue.
3. Which city has the largest tax percent/ VAT (Value Added Tax)?
4. Which customer type pays the most VAT?
### Customer Analysis
1. How many unique customer types does the data have?
2. How many unique payment methods does the data have?
3. Which is the most common customer type?
4. Which customer type buys the most?
5. What is the gender of most of the customers?
6. What is the gender distribution per branch?
7. Which time of the day do customers give most ratings?
8. Which time of the day do customers give most ratings per branch?
9. Which day of the week has the best avg ratings?
10. Which day of the week has the best average ratings per branch?



