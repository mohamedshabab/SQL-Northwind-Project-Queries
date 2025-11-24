# 🐘 Northwind SQL Analysis Project (MySQL)

This project explores the classic **Northwind** database using SQL queries focused on real-world data analysis.  
It includes hands-on practice with **SELECT statements, filtering, sorting, JOIN operations, GROUP BY aggregations, and subqueries**, using tasks completed from the Northwind exercises in the final workbook.

The goal of this project is to demonstrate practical SQL skills used in data analytics and relational database querying, supported with screenshots and short explanations.

-----

## 📁 Dataset Overview

This project is based on the **Northwind Database**, a well-known relational dataset modeling a wholesale trading company.  
The database includes customers, orders, products, employees, suppliers, and sales territories.  
I used it to practice SQL querying and explore real business scenarios.

### 📦 Key Tables Used

- 👥 **`Customers`** — customer information and locations  
- 🛍️ **`Orders`** — order dates and customer/employee references  
- 📦 **`Order_Details`** — quantities, discounts, and line-item pricing  
- 🏭 **`Products`** — product names, categories, suppliers  
- 🧑‍💼 **`Employees`** — staff information and territories  
- 🚚 **`Suppliers`** — supplier company details  
- 🌍 **`Territories` / `Regions`** — geographic sales assignments  

### 📄 Files Used

- *Northwind Database Basic Queries.sql*  
- *Northwind Classwork – Joins & Group By.sql*  
- *Northwind Database Create.sql*  
- Selected tasks from the **Week 3 Workbook** (Day 2 – Task 1, Day 3 – Task 2)

These files contain all SQL code executed for this project.

----

## 🎯 Project Objectives

The purpose of this SQL project is to build confidence working with structured datasets by writing practical queries across multiple related tables.

### **Key Objectives**
- Understand the structure of the Northwind relational schema  
- Retrieve data using `SELECT` and `FROM`  
- Filter records using `WHERE`  
- Sort results with `ORDER BY`  
- Limit output using `LIMIT`  
- Join tables using `INNER JOIN` and `LEFT JOIN`  
- Summarize data using `GROUP BY` and aggregate functions  
- Analyze real business scenarios:
  - top-selling products  
  - customer order history  
  - supplier-product relationships  
  - employee territory coverage 

---

## 🛠️ SQL Skills Practiced

Throughout this project, I strengthened my SQL fundamentals while exploring the Northwind dataset.

### 📌 Core SQL Concepts
- `SELECT` for column retrieval  
- `WHERE` for filtering rows  
- `ORDER BY` for sorting  
- `LIMIT` for restricting results  

### 🔗 Joins & Table Relationships
Worked extensively with multi-table queries using:
- `INNER JOIN`  
- `LEFT JOIN`

Connecting tables such as:
- `Customers` → `Orders`  
- `Orders` → `Order_Details`  
- `Products` → `Suppliers`  
- `Employees` → `Territories`  

### 🔢 Grouping & Aggregation
Used:
- `GROUP BY`  
- `SUM()`  
- `COUNT()`  
- `AVG()`  
- `MIN()` / `MAX()`

To answer real analytical questions, including:
- total orders per country  
- quantities sold per product  
- average pricing  
- category-specific product listings  

### 🧱 Schema Understanding
Reviewed:
- table creation  
- primary & foreign keys  
- relationships across the Northwind structure
- 
----

## 🔍 Analysis Highlights

Below are the key SQL exercises from the Northwind project, each demonstrating a specific query pattern.  
This section includes the actual SQL queries from your tasks (Day 2 & Day 3) written as clean SQL code blocks.
---

### 🧾 1. Basic SELECT Queries  
Showcases simple column selection and filtering from tables like `Customers`, `Products`, and `Orders`.

```sql
SELECT CustomerID,
       CompanyName,
       Country
FROM Customers;

```
### 🔗 2. INNER JOIN – Orders with Customers

Used to combine customer information with their orders.

```sql
SELECT Orders.OrderID,
       Customers.CompanyName,
       Orders.OrderDate
FROM Orders
INNER JOIN Customers
       ON Orders.CustomerID = Customers.CustomerID;


```
### 📦 3. JOIN Products → Suppliers

Links each product to the supplier that provides it.

```sql
SELECT ProductName,
       SupplierName
FROM products
JOIN suppliers
       ON products.SupplierID = suppliers.SupplierID;


```
### 🏷️ 4. JOIN Products → Categories

Finds the category of each product.

```sql
SELECT CategoryName,
       ProductName
FROM products
JOIN categories
       ON products.CategoryID = categories.CategoryID;


```
### 🍗 5. Category-Specific Product Report (Meat/Poultry)

Lists all products in the Meat/Poultry category.

```sql
SELECT ProductName,
       CategoryName
FROM products
JOIN categories
       ON products.CategoryID = categories.CategoryID
WHERE CategoryName = 'Meat/Poultry';

```
### 📊 6. GROUP BY – Total Quantity Ordered per Product

Aggregates total quantity ordered.

```sql
SELECT Products.ProductName,
       SUM(Order_Details.Quantity) AS TotalOrdered
FROM Order_Details
INNER JOIN Products
       ON Order_Details.ProductID = Products.ProductID
GROUP BY Products.ProductName;


```
### 🌍 7. Orders by Country

Counts orders grouped by customer country.

```sql
SELECT Customers.Country,
       COUNT(Orders.OrderID) AS NumberOfOrders
FROM Customers
INNER JOIN Orders
       ON Customers.CustomerID = Orders.CustomerID
GROUP BY Customers.Country
ORDER BY NumberOfOrders DESC;

```
### 👨‍💼 8. Employee Territory Lookup

Shows which employees manage which territories.

```sql
SELECT Employees.LastName,
       Territories.TerritoryDescription
FROM EmployeeTerritories
INNER JOIN Employees
       ON EmployeeTerritories.EmployeeID = Employees.EmployeeID
INNER JOIN Territories
       ON EmployeeTerritories.TerritoryID = Territories.TerritoryID;
```
----

## 🎓 Learning Outcomes

Through completing the Northwind SQL tasks, I developed several core data skills used in real-world analytics work:

### 🔹 SQL Query Writing  
- Extracted data using `SELECT`, `WHERE`, and column filtering  
- Joined multiple tables using `INNER JOIN`  
- Used aliases and table references for cleaner queries  

### 🔹 Relational Database Understanding  
- Worked with a multi-table schema (Customers, Orders, Products, Suppliers, Categories, Territories, Employees)  
- Understood how foreign keys connect data across the Northwind system  

### 🔹 Data Aggregation & Reporting  
- Applied `GROUP BY` to summarize product performance  
- Calculated totals such as **total quantity ordered**  
- Filtered category-specific product reports  

### 🔹 Business Insight Generation  
- Identified top-ordering countries  
- Connected products with suppliers and categories  
- Mapped employees to territories to analyze workforce coverage  

These SQL tasks demonstrate competency in querying relational databases, joining tables, aggregating data, and generating business-ready insights.

---

## 📌 Conclusion

The Northwind SQL project provides a practical demonstration of working with a real relational database.  
Through a series of structured SQL tasks, I explored how data is connected across customers, orders, products, employees, and regions.

By writing queries that included filtering, joining, grouping, and summarizing, I was able to generate meaningful business insights such as:

- Which countries place the most orders  
- Which products are ordered most frequently  
- How orders link to suppliers and categories  
- How employees and territories are structured  

Overall, this project strengthened my ability to work with SQL in a real-world, multi-table environment and improved my confidence in producing clear, accurate data reports using relational queries.

---

## 🖥️ How to Use This Project

This repository includes the SQL scripts used for the Northwind exercises:

- **northwind_create.sql** – creates and loads the database  
- **basic_queries.sql** – SELECT queries  
- **joins_groupby.sql** – JOIN and GROUP BY tasks  

### ✔️ Run the Project

1. Open MySQL Workbench / pgAdmin / SQL Server / Azure Data Studio  
2. Load the database:

   SOURCE northwind_create.sql;


