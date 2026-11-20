# Customer-Trend-data-analysis
# Customer Shopping Behavior Analysis

Data cleaning and feature engineering on 3,900 retail purchase records using Python and pandas, with the cleaned data loaded into PostgreSQL for SQL analysis.

## Overview
Retail teams need clean, structured data before they can study customer behaviour. This project prepares a customer shopping dataset for analysis and stores it in a relational database.

## Dataset
- 3,900 records, 18 columns
- Customer details (age, gender, location, subscription status), product details (item, category, size, colour, season), transaction details (purchase amount, review rating, shipping, discount, payment method) and behaviour (previous purchases, purchase frequency)

## What I did
- Found 37 missing Review Ratings and filled them with the median rating of each product category
- Standardised column names to snake_case
- Created `age_group` (quartile-based) and `purchase_frequency_days` (text frequency converted to days)
- Dropped `promo_code_used`, which was identical to `discount_applied`
- Loaded the final table into PostgreSQL using SQLAlchemy (MySQL and SQL Server connection code is also included)

## Tech stack
Python, pandas, SQLAlchemy, PostgreSQL, Jupyter Notebook

## How to run
1. Clone the repo and install dependencies: `pip install pandas sqlalchemy psycopg2-binary`
2. Place `customer_shopping_behavior.csv` in the project folder
3. Set your own database credentials (use environment variables, never commit passwords)
4. Run `Customer_Shopping_Behavior_Analysis.ipynb`

## Next steps
- SQL queries on revenue by category, age group and season
- Impact of discounts and subscriptions on spending
- Dashboard in Power BI or Tableau
