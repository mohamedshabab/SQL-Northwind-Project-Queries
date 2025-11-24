# 🐘 Northwind SQL Analysis Project (MySQL)

This project explores the classic **Northwind** database using SQL queries focused on real-world data analysis.  
It includes hands-on practice with **SELECT statements, filtering, sorting, JOIN operations, GROUP BY aggregations, and subqueries**, using tasks completed from the Northwind exercises in the final workbook.

The goal of this project is to demonstrate practical SQL skills used in data analytics and relational database querying, supported with screenshots and short explanations.

-----

## 📁 Database Overview

This project uses the classic **Northwind** database, which models a wholesale trading company.  
The dataset includes customers, employees, suppliers, products, and order processing tables.

### 🧱 Main Tables in the Northwind Database  
(All table names are italicized using backticks)

- ***`Customers`*** – customer names, contact info, location  
- ***`Employees`*** – staff roles, reporting structure  
- ***`Suppliers`*** – product suppliers and their details  
- ***`Products`*** – product names, prices, stock  
- ***`Categories`*** – product groupings  
- ***`Orders`*** – order header information  
- ***`Order_Details`*** – order line items  
- ***`Shippers`*** – shipping companies  
- ***`Territories`*** / ***`Regions`*** – geographic mapping  

### 📄 Files Used

- **Northwind Database Basic Queries.sql**  
- **Northwind Classwork Joins and Group By.sql**  
- **Northwind Database Create.sql**  
- Workbook tasks (Day 2 & Day 3)

These files contain all SQL code used in this project.

----

## 🎯 Project Objectives

The goal of this SQL project is to practice real-world data querying using the **Northwind** relational database.  
The exercises cover core SQL skills including filtering, sorting, grouping, joining tables, and writing multi-step analytical queries.

### **Key Objectives**
- Write queries to explore customers, orders, employees, products, and suppliers  
- Practice SQL fundamentals (SELECT, WHERE, ORDER BY, LIMIT)  
- Use **JOINs** to combine data across multiple tables  
- Apply **GROUP BY** and **aggregate functions** to summarize sales and inventory  
- Write queries using **HAVING**, **DISTINCT**, and **string filtering**  
- Solve analytical tasks from the *Day 2* and *Day 3* Northwind workbook exercises  
- Include screenshot examples in the README to demonstrate SQL results  

The project is designed to simulate tasks given to real data technicians or analysts working with relational databases.

----
## 🎯 Project Objectives

The goal of this SQL project is to practice core database querying skills using the **Northwind** dataset.  
The exercises focus on understanding relational data and writing practical SQL queries used in real business analytics.

### **Key Objectives**
- Understand the structure of the Northwind database (tables, relationships, primary/foreign keys)
- Use **SELECT** to retrieve specific columns from tables
- Use **FROM** to specify data sources
- Filter records with **WHERE**
- Sort results with **ORDER BY**
- Limit output using **LIMIT**
- Combine tables using **INNER JOIN** and **LEFT JOIN**
- Aggregate data using **GROUP BY** with functions like:
  - **COUNT()**
  - **SUM()**
  - **AVG()**
  - **MIN()**
  - **MAX()**
- Query real business data such as:
  - bestselling products  
  - customer order history  
  - supplier inventory  
  - employee–territory relationships
- Practice writing clean, readable, and efficient SQL queries

---

## 📁 Dataset Overview

This project is built using the **Northwind Database**, a classic relational dataset that contains information about customers, orders, products, employees, suppliers, and logistics operations.

You worked with three SQL task files from the training materials:

- **Northwind Database Basic Queries.sql**  
- **Northwind Classwork – Joins & Group By.sql**  
- **Northwind Database Create.sql** (schema reference)

You also used selected tasks from the workbook:
- **Northwind Day 2 – Task 1**  
- **Northwind Day 3 – Task 2**

Together, these exercises cover essential SQL topics using real-world business data.

### 📦 Key Tables in the Northwind Database

#### 👥 Customers  
Contains customer details such as company name, contact info, city, and country.

#### 🛍️ Orders  
Includes order dates, shipping details, employee handling, and customer linkage.

#### 📦 Order Details  
Line-level items showing product, quantity, price, and discount for each order.

#### 🏭 Products  
Contains product names, categories, suppliers, and stock information.

#### 🧑‍💼 Employees  
Stores employee names, roles, reporting structure, and territory assignments.

#### 🚚 Suppliers  
Information about suppliers providing products to the business.

#### 🌍 Territories & Regions  
Geographical categorization used for employee sales areas.

### 📄 Files Used in This Project

- `/mnt/data/Northwind Database Basic Queries.sql`
- `/mnt/data/Northwind Classwork Joins and Group By.sql`
- `/mnt/data/Northwind Database create (1).sql`
- Selected tasks from:  
  `/mnt/data/Data_Technician_Workbook_Week_3 Workbench use.docx`

These files were used to run and practice SQL queries throughout the project.

---

## 🛠️ SQL Skills Practiced

Throughout this project, you worked with the Northwind database to build confidence in real SQL query writing.  
The exercises covered essential SQL techniques used in everyday data analytics.

### 📌 Core SQL Concepts
- Selecting specific columns using **`SELECT`**
- Filtering rows using **`WHERE`**
- Sorting results with **`ORDER BY`**
- Limiting records using **`LIMIT`** (or database equivalent)

### 🔗 Joins & Relationships
Worked extensively with multi-table queries using:
- **`INNER JOIN`** – combining matching rows across tables  
- **`LEFT JOIN`** – returning all rows from a primary table  
- Joining tables such as:
  - `Customers` ↔ `Orders`  
  - `Orders` ↔ `Order_Details`  
  - `Products` ↔ `Suppliers`  
  - `Employees` ↔ `Territories`

### 🔢 Grouping & Aggregation
Performed grouped analytical queries using:
- **`GROUP BY`**
- **`COUNT()`**
- **`SUM()`**
- **`AVG()`**
- **`MIN()` / `MAX()`**

Used these to answer questions such as:
- Number of orders per customer  
- Total quantity ordered by product  
- Average unit price  
- Orders grouped by country  

### 🧱 Database Structure Exploration
From the schema file, you reviewed:
- Table creation SQL  
- Primary and foreign keys  
- Relationships between customers, orders, employees, and products

### 📝 Practical Exercises from Workbook
Included selected tasks from:
- **Day 2 – Task 1** (joins, grouping, totals)  
- **Day 3 – Task 2** (multi-table queries, sorting, filtering)

These exercises simulate real analyst questions applied to the Northwind dataset.

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
   ```sql
   SOURCE northwind_create.sql;


