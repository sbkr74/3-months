# **Today's Data Engineering Learning Plan (4 Hours)**  
**Current Level:** Beginner (Starting with **Week 1-2: Core Concepts & SQL**)  

## **📅 Today’s Focus:**  
- **Relational Database Fundamentals**  
- **SQL Basics (SELECT, WHERE, GROUP BY, JOINs)**  
- **Hands-on Exercises with a Real Dataset**  

---

## **⏰ Time Breakdown (4 Hours)**  

### **1️⃣ Hour 1: Theory & Setup (60 mins)**
- **Relational Database Concepts (30 mins)**  
  - Tables, rows, columns, primary/foreign keys  
  - Normalization (1NF, 2NF, 3NF)  
  - ACID properties  
- **Setting Up SQL Environment (30 mins)**  
  - Install PostgreSQL / MySQL (or use free cloud DB like ElephantSQL)  
  - Install a SQL client (DBeaver, pgAdmin, or VS Code + SQL extensions)  

### **2️⃣ Hour 2: SQL Basics (60 mins)**  
- **Writing Basic Queries**  
  - `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`  
  - Aggregations (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)  
  - `GROUP BY` and `HAVING`  
- **Exercise:**  
  - Download [Sample Database (e.g., Northwind or Sakila)](https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/)  
  - Run 10 basic queries (e.g., "Find top 5 customers by order count")  

### **3️⃣ Hour 3: SQL Joins & Intermediate Queries (60 mins)**  
- **Understanding JOINs**  
  - `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`  
  - Self-joins and multi-table joins  
- **Exercise:**  
  - Write 5 complex queries (e.g., "Find customers who never placed an order")  
  - Optimize a slow query using `EXPLAIN ANALYZE`  

### **4️⃣ Hour 4: Mini-Project (60 mins)**  
- **Build a Small ETL Pipeline**  
  - Download a CSV dataset (e.g., [Kaggle Sales Data](https://www.kaggle.com/datasets))  
  - Load it into your database using Python (`pandas + sqlalchemy`)  
  - Write SQL queries to analyze it  

---

## **🎯 Today’s Challenges (What You Might Face)**  
1. **SQL Syntax Errors** → Use documentation (PostgreSQL / MySQL official docs).  
2. **JOIN Confusion** → Draw table relationships on paper first.  
3. **Slow Queries** → Learn indexing basics (tomorrow’s topic).  

## **📌 Tomorrow’s Preview:**  
- **Indexes & Query Optimization**  
- **Working with Larger Datasets**  
- **Introduction to Python for ETL**  

---

### **💡 Pro Tip:**  
- If stuck, check [SQLZoo](https://sqlzoo.net/) or [LeetCode SQL Problems](https://leetcode.com/problemset/database/).  
- Keep a **learning log** (what worked, what didn’t).  

---
# **Ultra-Specific Daily Data Engineering Plan (Day 1 - SQL Fundamentals)**  
**Focus:** Relational Databases & Core SQL (4 Hours)  
**Format:** Tasks → Subtasks → Check Questions → Challenges → Tricky Problems  

---

## **🔥 Hour 1: Database Fundamentals & Setup**  

### **📌 Tasks:**  
1. **Understand Relational Databases (30 mins)**  
   - Subtask 1: Watch [What is a Relational Database?](https://youtu.be/OqjJjpjDRLc) (10 mins)  
   - Subtask 2: Draw a simple **3-table schema** (Users, Orders, Products) with PKs/FKs (15 mins)  
   - Subtask 3: Explain **normalization** (1NF, 2NF, 3NF) in your own words (5 mins)  

2. **Setup SQL Environment (30 mins)**  
   - Subtask 1: Install [PostgreSQL](https://www.postgresql.org/download/) (15 mins)  
   - Subtask 2: Install [DBeaver](https://dbeaver.io/) (10 mins)  
   - Subtask 3: Load the [Northwind DB](https://github.com/pthom/northwind_psql) (5 mins)  

### **❓ Check Questions:**  
- *"Why do we need foreign keys?"*  
- *"What happens if a table isn’t in 1NF?"*  
- *"What’s the difference between DBeaver and pgAdmin?"*  

### **💡 Challenge:**  
- **Spot the Error:** You designed a table with columns: `OrderID, ProductName, CustomerName, CustomerAddress`. Why is this problematic?  

### **🎯 Tricky Question:**  
- *"Can a table have multiple primary keys? If yes, how?"*  

---

## **🔥 Hour 2: SQL Basics (SELECT, WHERE, GROUP BY)**  

### **📌 Tasks:**  
1. **Write 10 Basic Queries (30 mins)**  
   - Subtask 1: `SELECT * FROM customers WHERE country = 'Germany';`  
   - Subtask 2: `SELECT product_name, unit_price FROM products WHERE unit_price > 20;`  
   - Subtask 3: `SELECT country, COUNT(*) FROM customers GROUP BY country;`  

2. **Aggregations (30 mins)**  
   - Subtask 1: Find the **average** order quantity.  
   - Subtask 2: List **top 5 most expensive products**.  
   - Subtask 3: Count orders **per customer** (hint: `GROUP BY`).  

### **❓ Check Questions:**  
- *"When would you use HAVING vs WHERE?"*  
- *"What’s the difference between COUNT(*) and COUNT(column_name)?"*  

### **💡 Challenge:**  
- **Debug This:**  
  ```sql
  SELECT customer_id, COUNT(*) 
  FROM orders 
  WHERE COUNT(*) > 5 
  GROUP BY customer_id;
  ```
  *(Why does this fail? Fix it.)*  

### **🎯 Tricky Question:**  
- *"How would you find customers who haven’t placed any orders?"*  

---

## **🔥 Hour 3: SQL JOINs (INNER, LEFT, RIGHT, FULL)**  

### **📌 Tasks:**  
1. **Write 5 JOIN Queries (30 mins)**  
   - Subtask 1: `INNER JOIN` orders + customers → Get order details with customer names.  
   - Subtask 2: `LEFT JOIN` products + categories → Show all products (even uncategorized).  
   - Subtask 3: `SELF JOIN` employees → Find who reports to whom.  

2. **Multi-Table JOIN (30 mins)**  
   - Subtask 1: Join **orders + customers + order_details + products** → Get revenue per customer.  
   - Subtask 2: Find **suppliers who provide no products** (hint: `LEFT JOIN + WHERE IS NULL`).  

### **❓ Check Questions:**  
- *"What’s the difference between INNER and LEFT JOIN?"*  
- *"When would you use a FULL JOIN?"*  

### **💡 Challenge:**  
- **Optimize This:**  
  ```sql
  SELECT * 
  FROM orders 
  WHERE order_date BETWEEN '1996-01-01' AND '1996-12-31';
  ```
  *(How would you make this faster? Hint: Indexes.)*  

### **🎯 Tricky Question:**  
- *"How would you find duplicate rows in a table?"*  

---

## **🔥 Hour 4: Mini-Project (ETL with Python + SQL)**  

### **📌 Tasks:**  
1. **Load CSV into DB (30 mins)**  
   - Subtask 1: Download [Sample Sales Data CSV](https://www.kaggle.com/datasets).  
   - Subtask 2: Use Python (`pandas + sqlalchemy`) to load it into PostgreSQL.  

2. **Analyze Data with SQL (30 mins)**  
   - Subtask 1: Find **total sales by region**.  
   - Subtask 2: Identify **best-selling products**.  
   - Subtask 3: Detect **outliers** (e.g., orders with abnormally high quantities).  

### **❓ Check Questions:**  
- *"Why use SQL instead of pandas for analysis?"*  
- *"What’s the risk of loading raw CSV data directly?"*  

### **💡 Challenge:**  
- **Data Quality Check:** Write a SQL query to find **NULL values** in critical columns.  

### **🎯 Tricky Question:**  
- *"How would you handle a CSV with 10M rows without crashing your system?"*  

---

## **✅ End-of-Day Review**  
- **What did you learn?** (Write 3 bullet points)  
- **What was confusing?** (Identify gaps for tomorrow)  
- **What’s next?** (Indexes & query optimization!)  
