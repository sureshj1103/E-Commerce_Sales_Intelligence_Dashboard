# E-Commerce_Sales_Intelligence_Dashboard
 Analyzed e-commerce sales data to create an attractive sales dashboard using Power BI

## 🛍 Project Title
E-Commerce Sales Intelligence Dashboard

## 📌 Brief One-Line Summary
An advanced sales intelligence dashboard project leveraging real e-commerce data to uncover business-driving insights using Python, SQL, and Power BI.

## 🧠 Overview
This project simulates a real-world sales analysis scenario for an e-commerce company, covering the full data pipeline: ingestion, cleaning, modeling, analysis, and dashboard creation. Designed to support business decisions with meaningful KPIs like customer performance, sales trends, profit metrics, and geographic segmentation.

## ❓ Problem Statement
E-commerce businesses handle vast, complex transactional data but often lack the tools and processes to extract strategic value. This project provides a reusable analytical framework to turn sales data into insights for informed decision-making.

## 📦 Dataset
Orders.csv — Order-level data including Order ID, Date, Customer, State, Amount, and Profit.

Details.csv — Product-level data with Category, Sub-Category, Quantity, Payment Mode, and Average Order Value.

## 🛠 Tools and Technologies
Excel for data cleaning
MySQL for relational storage and querying
Power BI for advanced dashboarding

## ⚙️ Methods
1. Data Ingestion
2. Data Cleaning
Handled missing values
Converted date fields to datetime
Cleaned inconsistent state and category entries
Ensured numeric types for sales/profit columns
# 3. Database Design (MySQL Schema)
sql
Copy
Edit
CREATE TABLE Orders (
    order_id VARCHAR(20) PRIMARY KEY,
    order_date DATE,
    customer_name VARCHAR(100),
    state VARCHAR(100),
    amount DECIMAL(10, 2),
    profit DECIMAL(10, 2)
);

CREATE TABLE OrderDetails (
    order_id VARCHAR(20),
    category VARCHAR(50),
    sub_category VARCHAR(50),
    quantity INT,
    payment_mode VARCHAR(50),
    avg_order_value DECIMAL(10, 2),
    FOREIGN KEY (order_id) REFERENCES Orders(order_id)
);
4. Load Data into MySQL
5. Power BI Dashboard
Connected to MySQL

## Created interactive visuals:

📈 Profit by Month
📍 Amount by State (Map)
📊 Profit by Category/Sub-Category
🛒 Top 5 Customers by Sales
💳 Payment Mode Distribution
📦 Quarterly Sales Analysis

## 🔑 Key Insights and Outcomes
Clothing and Electronics dominate profit share (>70%)
COD remains the most used payment method (~34%)
Maharashtra and Delhi lead in total sales
The top 10 customer accounts for a significant portion of revenue
Strong seasonal trends noted in Q2 and Q4

## 📊 Dashboard/Model/Output
Dashboard built in Power BI with slicers for:

Quarter
State
Category
KPIs like total amount, profit, order quantity, average order value
Drill-down support for customer-level exploration

<img width="1341" height="761" alt="image" src="https://github.com/user-attachments/assets/58d7c2ac-a758-4ec4-b4b9-8551b3f41670" />


## 🧾 Results & Conclusion
This dashboard project distills large-scale transactional data into a clear narrative of customer behavior, payment preferences, and category performance. It delivers fast, intuitive insights for managers and marketing teams alike.




## 🔮 Future Work
Add predictive models (e.g., sales forecasting)
Integrate customer segmentation using clustering
Automate dashboard refresh via Power BI Service
Add anomaly detection for returns or fraudulent orders
