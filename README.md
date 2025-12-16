# 🍽️ Zomato Food Orders Analysis  
### SQL • Python • Power BI | End-to-End Data Analytics Project

An **end-to-end data analytics project** analyzing **1.25 lakh+ Zomato food orders** to uncover insights related to **city performance, restaurant revenue, food item popularity, and customer spending behavior**.

---

## 📌 Project Overview

## 📊 Power BI Dashboard Preview

### 🔹 Executive Overview
<p align="center"><img width="800" src="https://github.com/user-attachments/assets/fd9b9907-7dad-4ca4-9c8f-9443e28b7939" /></p> <br>

### 🔹 City & Restaurant Analysis
<p align="center"><img width="800" src="https://github.com/user-attachments/assets/3b7ef277-b865-46c7-8b75-47d28f1cd475" /></p> <br>

### 🔹 Food Item Insights
<p align="center"><img width="800" src="https://github.com/user-attachments/assets/225977a2-86d9-4aea-b5d3-488c0f21a0ad" /></p> <br>


The objective of this project is to analyze Zomato order data and answer key business questions such as:

- Which cities generate the highest revenue?
- Which restaurants contribute the most to sales?
- Which food items perform best by revenue and AOV?
- How does pricing impact overall revenue?

The original dataset contained **6.4 lakh+ raw records**, which were cleaned and standardized to **1.25 lakh high-quality records** for accurate analysis.

---

## 🛠️ Tech Stack Used

- **Python (Pandas, Regex)** – Data cleaning & feature extraction  
- **SQL (MySQL)** – Business queries & aggregations  
- **Power BI** – Interactive dashboards & visual insights  
- **Excel / Power Query** – Initial exploration & validation  

---

## 🧹 Data Cleaning & Preparation

### Key cleaning steps performed:

- Extracted **food_item** and **order_value** from raw `order_item` text
- Removed rows with missing or invalid prices
- Standardized city and restaurant names
- Reduced dataset size from **6.47L → 1.25L rows** for reliable insights

> 📌 This reflects a real-world scenario where raw business data must be cleaned before meaningful analysis.

---

## 🗄️ Database Schema (MySQL)

CREATE TABLE zomato_orders (
    city VARCHAR(100),
    order_item TEXT,
    order_restaurant VARCHAR(255),
    order_value DECIMAL(10,2),
    food_item VARCHAR(150)
);
📊 SQL Analysis Performed
Business questions answered using SQL:

Total Orders & Total Revenue

City-wise Orders and Revenue

Top Restaurants by Revenue

Most Popular Food Items

Average Order Value (AOV)

Sample Query:

SELECT 
    city,
    SUM(order_value) AS revenue
FROM zomato_orders
GROUP BY city
ORDER BY revenue DESC;

📈 Power BI Dashboard
🔹 Page 1: Executive Overview

Total Orders

Total Revenue

Unique Cities

Average Order Value (AOV)

Top Cities by Revenue & Orders

🔹 Page 2: City & Restaurant Analysis

City-wise performance table

Top restaurants by revenue

Total orders by restaurant

City slicer for interactive analysis

🔹 Page 3: Food Item Insights

Top 10 food items by Total Revenue

AOV by food item

City-wise food performance

📌 Important Insight:
Many food items had similar order volumes, so revenue and AOV were used instead of order count to avoid misleading rankings.

🔍 Key Insights

New Delhi, Chennai, and Bangalore are the top revenue-generating cities

Some food items generate high revenue due to premium pricing, not order volume

High-AOV items significantly impact total revenue

Order count alone is not always a reliable ranking metric

🎯 Business Value

This analysis helps stakeholders to:

Identify high-value cities and restaurants

Understand pricing vs volume impact

Optimize menu pricing strategies

Enable data-driven decision making
