# De-analyst-
# 🧾 Customer Purchase Analysis (SQL Project)

This is a beginner-friendly SQL project where I analyze sales data for an electronics store using SQL queries.

## 📌 Project Objective

The goal of this project is to:
- Calculate total revenue from each order
- Identify top spending customers
- Analyze product trends
- Filter and sort data for insights

## 🗃️ Dataset

The dataset used in this project is a manually created table named `orders`, which simulates customer purchase data.

### Table: `orders`

| order_id | customer_name | product     | quantity | price_per_unit | order_date  |
|----------|----------------|-------------|----------|----------------|-------------|
| 1        | Alice          | Laptop      | 1        | 300000         | 2023-01-05  |
| 2        | Bob            | Phone       | 2        | 120000         | 2023-02-10  |
| 3        | Cynthia        | Tablet      | 1        | 150000         | 2023-03-15  |
| 4        | Alice          | Headphones  | 3        | 10000          | 2023-03-18  |
| 5        | Daniel         | Phone       | 1        | 120000         | 2023-04-01  |
| 6        | Cynthia        | Laptop      | 1        | 300000         | 2023-04-10  |
| 7        | Bob            | Tablet      | 2        | 150000         | 2023-05-01  |
| 8        | Esther         | Phone       | 3        | 120000         | 2023-05-12  |

## 📊 Key SQL Queries

### 1. Calculate total cost per order
```sql
SELECT 
  order_id, customer_name, product, quantity, price_per_unit,
  quantity * price_per_unit AS total_cost
FROM orders;

**2. Top 3 highest spending orders**
SELECT order_id, customer_name, product, quantity, price_per_unit,
quantity* price_per_unit AS total_cost
FROM orders
ORDER total_cost DESC
LIMIT 3;
