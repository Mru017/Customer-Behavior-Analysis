# Customer Shopping Behavior Analysis 🛍️

## Project Overview

This project analyzes customer shopping behavior using transactional data from 3,900 purchases across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

## Dataset Summary

- Rows: 3,900
- Columns: 18
-Key Features: Customer ID, Age, Gender, Item Purchased, Category, Purchase Amount, Location, Size, Color, Season, Review Rating, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Payment Method, Frequency of Purchases.

## Data Handling:
- Imputed missing values in Review Rating using category medians.

## Tech Stack & Methodology

1. Python (Data Cleaning & Feature Engineering)
- Used pandas for initial data preparation:
- Renamed columns to snake_case for consistency.
- Imputation: Handled missing values in review ratings.
- Feature Engineering: Created age_group (Young Adult, Middle-aged, Senior) and standardized purchase_frequency.
- Database Connection: Integrated with PostgreSQL to load the cleaned data.

2. SQL (Exploratory Data Analysis)
- Performed structured queries in PostgreSQL to answer key business questions:
- Revenue by Gender: Analyzed spending gaps between male and female customers.
- Shipping Analysis: Compared average purchase amounts between Standard and Express shipping.
- Segmentation: Classified customers into 'Loyal', 'New', and 'Returning' based on purchase history.
- Product Performance: Identified top-rated products and those most dependent on discounts.

3. Power BI (Dashboarding)

- Built an interactive dashboard to visualize the findings, featuring:
- Subscription status breakdown (27% Subscribers vs 73% Non-subscribers).
- Revenue by Age Group and Category.
- Filterable views by Shipping Type and Gender.

## Key Insights

- Gender Gap: Male customers generated significantly higher total revenue ($157k) compared to Female customers ($75k).
- Top Products: Items like Gloves, Sandals, and Boots hold the highest average ratings (>3.8).
- Age Demographics: The "Young Adult" group contributes the highest total revenue ($62k), followed closely by Middle-aged customers.
- Subscription Behavior: Subscribers make up only 27% of the base, but 958 repeat buyers are active subscribers, indicating a correlation between loyalty and subscription.
- Shipping: There is a negligible difference in average spend between "Standard" ($58.46) and "Express" ($60.48) shipping users.

## Business Recommendations

- Boost Subscriptions: Develop exclusive campaigns for the 73% non-subscriber base, perhaps offering "Express Shipping" as a perk, as spend behavior is similar.
- Loyalty Programs: Target the "Returning" segment with incentives to convert them into "Loyal" customers (currently 3,116 customers are flagged as Loyal).
- Targeted Marketing: Focus ad spend on Young Adults and Male demographics as they are the highest revenue drivers.
- Product Positioning: Highlight high-rated items (Gloves, Sandals) in marketing materials to build trust with new customers.

🚀 How to Run

- Python: Run python/data_cleaning.py to process the raw CSV.
- SQL: Import the cleaned data into PostgreSQL and run sql/analysis_queries.sql.
- Power BI: Open dashboard/shopping_insights.pbix to view the visualizations.


