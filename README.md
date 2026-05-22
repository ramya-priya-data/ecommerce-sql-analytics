# 🛒 E-Commerce Sales Analytics

A end-to-end SQL analytics project that analyzes an e-commerce dataset to extract actionable business insights across sales, customers, products, regions, returns, and advanced analytics.

---

## 📌 Project Overview

This project simulates a real-world e-commerce analytics workflow using MySQL. It covers 7 analytical domains with 30+ queries — ranging from basic aggregations to advanced window functions and customer segmentation models used in the industry.

---

## 🗃️ Database Schema

The database consists of 5 interrelated tables:

```
Regions ◄──── Customers ◄──── Orders ◄──── OrderDetails
                                               │
                                            Products
```

| Table | Description |
|---|---|
| `Regions` | Region and country information |
| `Customers` | Customer details with region mapping |
| `Products` | Product catalog with category and price |
| `Orders` | Order transactions with return status |
| `OrderDetails` | Line items linking orders to products |

---

## 📊 Business Questions Answered

### 1. General Sales Insights
- Total revenue generated over the entire period
- Revenue excluding returned orders
- Revenue breakdown by year, month, product and category
- Average Order Value (AOV) overall and by month
- Average order size by region

### 2. Customer Insights
- Top 10 customers by total revenue spent
- Repeat customer rate
- Average time between orders region-wise
- Customer segmentation — Platinum, Gold, Silver, Bronze
- Customer Lifetime Value (CLV)

### 3. Product & Order Insights
- Top 10 most sold products by quantity and by revenue
- Products with highest return rate
- Return rate by category
- Average product price per region
- Sales trend per product category

### 4. Temporal Trends
- Monthly sales trends over the past year
- AOV change by month

### 5. Regional Insights
- Regions with highest and lowest order volume
- Revenue comparison across all regions
- Combined order volume and revenue by region

### 6. Return & Refund Insights
- Overall return rate by product category
- Return rate by region
- Customers making the most frequent returns

### 7. Advanced Analytics
- Month-over-Month (MoM) Revenue Growth %
- Running Total of Revenue Over Time
- Product Performance Ranking within Each Category
- Customer Cohort Retention Analysis
- RFM Analysis — Recency, Frequency, Monetary

---

## 🔑 SQL Concepts Used

| Concept | Usage |
|---|---|
| Multi-table JOINs | Up to 5 tables joined in a single query |
| Window Functions | `LAG()`, `RANK()`, `SUM() OVER()`, `NTILE()` |
| CTEs | Used across 8+ queries for clean, readable logic |
| Subqueries | Correlated and derived table subqueries |
| Date Functions | `DATEDIFF`, `DATE_FORMAT`, `DATE_SUB`, `LAG` for time-series |
| CASE WHEN | Customer segmentation and RFM labeling |
| Aggregate Functions | `SUM`, `COUNT`, `AVG`, `MIN`, `MAX` with `GROUP BY` |
| PARTITION BY | Product ranking within each category independently |

---

## 🚀 Advanced Analytics Highlights

### 📈 Month-over-Month Revenue Growth
Tracks how revenue changes each month compared to the previous month using `LAG()` window function.

### 📊 Running Total of Revenue
Calculates cumulative revenue month by month using `SUM() OVER()` — shows business growth trajectory.

### 🏆 Product Ranking within Category
Ranks every product by revenue within its own category using `RANK() OVER (PARTITION BY Category)`.

### 👥 Customer Cohort Retention
Groups customers by their first order month and tracks how many return in subsequent months — reveals customer loyalty trends.

### 💎 RFM Analysis
Industry-standard customer segmentation model scoring every customer on:
- **Recency** — how recently they ordered
- **Frequency** — how many times they ordered
- **Monetary** — how much they spent

Customers are labeled as **Champion**, **Loyal Customer**, **At Risk High Value**, **Lost Customer**, or **Needs Attention** using `NTILE(3)` scoring.

---

## 📁 File Structure

```
ecommerce-sales-analytics/
│
├── E-Commerce_Sales_Analytics.sql   # Complete project file
│   ├── CREATE DATABASE
│   ├── CREATE TABLE (5 tables)
│   ├── INSERT INTO (sample data)
│   └── Analytical Queries (Section 1–7)
│
└── README.md
```

---

## ▶️ How to Run

1. Open **MySQL Workbench**
2. Click **File** → **Open SQL Script**
3. Select `E-Commerce_Sales_Analytics.sql`
4. Press **Ctrl + Shift + Enter** to run the entire file
5. The database, tables, data and all queries will execute automatically

---

## 🛠️ Tools & Technologies

![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-Analytics-orange?style=for-the-badge)

---

