# customer_behavior_analysis

 Customer Shopping Behavior Analysis
 
🧭Overview

This project presents a complete data analytics pipeline analyzing customer shopping behavior using transaction-level data. It explores how demographics, product categories, discounts, and subscriptions influence spending.

The workflow integrates Python (EDA & Cleaning), SQL (Business Queries), and Power BI (Visualization) to deliver actionable business insights and recommendations.

📊 Dataset

Dataset Summary

Rows: 3,900

Columns: 18


Key Features:

🧑‍🤝‍🧑 Demographics: Age, Gender, Location, Subscription Status

🛒 Purchase Details: Item Purchased, Category, Purchase Amount, Season, Size, Color

💳 Shopping Behavior: Discount Applied, Promo Code Used, Review Rating, Shipping Type

Missing Values: 37 in the Review Rating column (handled via median imputation)

Average Purchase Amount: $59.76

Age Range: 18 to 70 years


🧰 Tools & Technologies
Category	Tools / Libraries
Programming & Data Analysis	Python (Pandas, NumPy, Matplotlib, Seaborn)
Database Management	PostgreSQL / MySQL / SQL Server
Data Visualization	Power BI
Reporting	Gamma App
Environment	Jupyter Notebook / VS Code

⚙️ Project Workflow
1️⃣ Data Preparation in Python

Loaded dataset using pandas

Explored structure and summary statistics (.info(), .describe())

Detected missing values and handled them appropriately


2️⃣ Data Cleaning & Feature Engineering

Imputed missing ratings with category-wise median values

Standardized column names to snake_case

Created new columns:

age_group (Young Adult, Adult, Middle-aged, Senior)

purchase_frequency_days (derived from transaction timestamps)

Checked redundancy between discount_applied and promo_code_used (removed one)


3️⃣ SQL-Based Business Insights

After cleaning, the dataset was uploaded to PostgreSQL for deeper business analysis.

Key SQL queries answered:

Question	Description
1. Revenue by Gender	Compared total purchase amounts across male and female customers.
2. High-Spending Discount Users	Found customers using discounts but spending above average.
3. Top-Rated Products	Identified products with highest average review scores.
4. Shipping Type Analysis	Compared spending across different shipping options.
5. Subscribers vs. Non-Subscribers	Measured spending differences by subscription status.
6. Discount-Dependent Products	Highlighted products most often sold at a discount.
7. Customer Segmentation	Grouped customers into New, Returning, and Loyal segments.
8. Top Products per Category	Listed top-selling products by category.
9. Repeat Buyers & Subscriptions	Checked whether repeat buyers were more likely to subscribe.
10. Revenue by Age Group	Calculated total contribution by age segments.

    
📈 Power BI Dashboard

The Power BI dashboard visualizes the findings with interactive filters for Subscription, Gender, Category, and Shipping Type.

📸 Dashboard Preview:

Dashboard Highlights:

Total Customers: 627

Average Purchase Amount: $60.73

Average Review Rating: 3.77

Subscription Share: 24.4% Subscribers, 75.6% Non-Subscribers

Top Categories by Revenue: Clothing → Accessories → Footwear

Young Adults lead in both sales and revenue


💡 Key Insights

Clothing is the highest revenue-generating category.

Male customers contributed higher total revenue.

Subscribers spend significantly more per transaction.

Discounts improve sales volume but lower profit margins.

Young adults are the most valuable customer segment.


🧩 Business Recommendations

Promote Subscriptions: Offer incentives for regular buyers.

Loyalty Programs: Reward repeat customers to increase retention.

Optimize Discount Strategy: Balance discount offers with margin protection.

Highlight Top Products: Feature best-rated items in marketing campaigns.

Targeted Marketing: Focus ads on high-value age groups and express shipping users.




🚀 Future Enhancements

Automate Power BI data refresh via cloud connection

Add predictive modeling for customer churn and next purchase

Build a Streamlit dashboard for interactive web analytics

