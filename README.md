# E-COMMERCE-CHURN-ANALYSIS---SQL-
SQL-based E-Commerce Customer Churn Analysis using data cleaning, transformation, and customer behavior analysis.

# E-Commerce Customer Churn Analysis

## Project Overview

This project focuses on analyzing customer churn in an e-commerce dataset using SQL.

The project includes data cleaning, data transformation, and SQL-based data exploration to understand customer behavior, churn patterns, payment preferences, order activity, customer satisfaction, and returns.

## Objectives

- Analyze active and churned customers.
- Identify customer churn patterns.
- Analyze customer tenure and cashback.
- Study customer complaints and satisfaction.
- Analyze preferred payment methods and order categories.
- Examine coupon usage and order activity.
- Analyze warehouse-to-home distance and churn status.
- Combine customer and return data for further analysis.

## Database

**Database Name:** `ecomm`

**Main Table:** `customer_churn`

**Additional Table:** `customer_returns`

## Data Cleaning

The following data-cleaning operations were performed:

- Missing `WarehouseToHome` values were imputed using the mean.
- Missing `HourSpendOnApp` values were imputed using the mean.
- Missing `OrderAmountHikeFromlastYear` values were imputed using the mean.
- Missing `DaySinceLastOrder` values were imputed using the mean.
- Missing `Tenure`, `CouponUsed`, and `OrderCount` values were imputed using the mode.
- Outliers in `WarehouseToHome` greater than 100 were removed.
- `Phone` was replaced with `Mobile Phone`.
- `Mobile` was replaced with `Mobile Phone`.
- `COD` was replaced with `Cash on Delivery`.
- `CC` was replaced with `Credit Card`.

## Data Transformation

The following transformations were performed:

- Renamed `PreferedOrderCat` to `PreferredOrderCat`.
- Renamed `HourSpendOnApp` to `HoursSpentOnApp`.
- Created `ComplaintReceived` based on the `Complain` column.
- Created `ChurnStatus` based on the `Churn` column.
- Removed the original `Churn` and `Complain` columns after creating the new status columns.

## SQL Analysis

The project includes SQL queries to analyze:

1. Active and churned customers
2. Average tenure and total cashback of churned customers
3. Percentage of churned customers who complained
4. City tier with the highest churned customers for Laptop & Accessory
5. Most preferred payment mode among active customers
6. Order amount hike for single customers preferring mobile phones
7. Average devices registered among UPI users
8. City tier with the highest number of customers
9. Gender with the highest coupon usage
10. Customer count and maximum app usage by order category
11. Total order count of Credit Card users with maximum satisfaction
12. Average satisfaction score of customers who complained
13. Preferred order category among customers using more than 5 coupons
14. Top 3 order categories by average cashback
15. Payment modes of customers based on tenure and order count
16. Warehouse-to-home distance categorization and churn analysis
17. Customer order details based on marital status, city tier, and order count
18. Customer returns analysis using table joins

## Technologies Used

- MySQL
- SQL
- GitHub

## Key SQL Concepts Used

- `SELECT`
- `WHERE`
- `GROUP BY`
- `ORDER BY`
- `COUNT()`
- `SUM()`
- `AVG()`
- `MAX()`
- `ROUND()`
- `CASE`
- Subqueries
- `JOIN`
- `ALTER TABLE`
- `UPDATE`
- `DELETE`
- `CREATE TABLE`
- `INSERT INTO`

## Project Structure

```text
E-Commerce-Customer-Churn-Analysis/
│
├── E-Commerce Customer churn db.sql
└── README.md
