# SQL-Intern-task-5 : SQL Joins (Inner, Left, Right, Full)

## Objectives 
To understand and practices how to combine data from multiple tables using various types SQL joins.

## Tools used 
-DB Browser for SQLite *( for INNER and LEFT JOIN, and FULL JOIN simulation)*
-MySQL Workbench *( for all JOIN types including RIGHT and FULL JOIN)*

## Task Description

In this task, I created two related tables:
- **Customers** (customer_id, name, city)
- **Orders** (order_id, customer_id, product)

Using these tables, I explored the following SQL JOIN types:
- `INNER JOIN`
- `LEFT JOIN`
- `RIGHT JOIN` *(only in MySQL)*
- `FULL JOIN` *(simulated in SQLite using LEFT JOIN + UNION)*

## Sample SQL Queries

**INNER JOIN**

SELECT Customers.name, Orders.product
FROM Customers
INNER JOIN Orders ON Customers.customer_id = Orders.customer_id;

**LEFT JOIN**

SELECT Customers.name, Orders.product
FROM Customers
LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id;

**RIGHT JOIN (MySQL only)**

SELECT Customers.name, Orders.product
FROM Customers
RIGHT JOIN Orders ON Customers.customer_id = Orders.customer_id;

**FULL JOIN (Simulated in SQLite)**

SELECT Customers.customer_id, Customers.name, Orders.order_id, Orders.product
FROM Customers
LEFT JOIN Orders ON Customers.customer_id = Orders.customer_id

UNION

SELECT Orders.customer_id, Customers.name, Orders.order_id, Orders.product
FROM Orders
LEFT JOIN Customers ON Customers.customer_id = Orders.customer_id;

**Outcome: Mastery of Merging Data**
## Different SQL JOIN operations:

1.How to retrieve data from multiple related tables

2.How to handle unmatched records using LEFT and FULL JOINs

3.How to simulate unsupported JOINs in SQLite

## Deliverables:

1.SQL script for table creation and data insertion

2.JOIN queries using INNER, LEFT, RIGHT (MySQL), and simulated FULL JOIN


