# Jensen's SQL Dataset Analysis

## Project Overview
This project focuses on analyzing Jensen's dataset to gain insights into customer behavior, staff performance, inventory management, and store operations. Advanced SQL queries are used to uncover key metrics and provide actionable insights for decision-making.

---

## Dataset
**Source:** [Jensen's SQL Dataset](https://drive.google.com/drive/folders/1feFkClnYME7Be3kjmz-TD2PV1uVkXNAN)

---

## Objectives

### Queries Implemented:
1. **Find the total number of products sold by each store along with the store name.**
2. **Calculate the cumulative sum of quantities sold for each product over time.**
3. **Find the product with the highest total sales (quantity * price) for each category.**
4. **Find the customer who spent the most money on orders.**
5. **Find the highest-priced product for each category name.**
6. **Find the total number of orders placed by each customer per store.**
7. **List the names of staff members who have not made any sales.**
8. **Find the top 3 most sold products in terms of quantity.**
9. **Find the median value of the price list.**
10. **List all products that have never been ordered (using EXISTS).**
11. **List the names of staff members who have made more sales than the average number of sales by all staff members.**
12. **Identify the customers who have ordered all types of products (i.e., from every category).**

---

## Features
- **Customer Insights**: Analyze purchasing patterns and identify top customers.
- **Staff Performance**: Measure sales performance and identify underperforming staff.
- **Inventory Management**: Track product popularity and stock utilization.
- **Store Operations**: Monitor store-specific sales and activity.

---

## Setup Instructions

1. **Database Configuration**:
   - Load the dataset into your SQL environment (e.g., MySQL, PostgreSQL).
   - Create tables as per the dataset schema.

2. **Run Queries**:
   - Execute the provided SQL queries to generate insights.

3. **Software Requirements**:
   - SQL database (MySQL/PostgreSQL recommended).
   - SQL client (e.g., DBeaver, MySQL Workbench, or pgAdmin).

---

## Sample Query

Here’s an example query to find the total number of products sold by each store along with the store name:

```sql
SELECT store_id, store_name, SUM(quantity) AS total_products_sold
FROM sales
JOIN stores ON sales.store_id = stores.id
GROUP BY store_id, store_name;
