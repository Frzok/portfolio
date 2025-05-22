# 📄 Assignment

**Formatting requirement:**  
All results must be compiled into a single file, without references or links to other resources.  
The only exception: if you choose to describe the REST API using Swagger, it may be submitted as a separate file.

---

## 1. Databases – Quiz

For each of the following questions, select the correct statements. One or more statements may be correct.

**1** Does a table without any fields contain any information?

1. Contains information about the structure of the database  
2. Does not contain any information  
3. A table without fields cannot exist  
4. Contains information about future records  

**2** A record in a relational database file can contain:

1. Only homogeneous data (same type)  
2. Only text data  
3. Only boolean values  
4. Heterogeneous data (different types)  
5. Only numerical data  

**3** What is the difference between a primary key and a foreign key?

1. A primary key always consists of multiple columns, a foreign key only one  
2. Primary key values must be unique and non-null; foreign key values may repeat  
3. A foreign key identifies a row, and a primary key links tables  
4. A primary key identifies a row; a foreign key is used to link tables  

**4** Which normal form requires that all attributes depend on the whole primary key and not just a part of it?

1. 1NF  
2. 2NF  
3. 3NF  
4. 4NF  

**5** What is the execution order of SELECT, FROM, and GROUP BY in SQL?

1. SELECT → FROM → GROUP BY  
2. GROUP BY → SELECT → FROM  
3. FROM → SELECT → GROUP BY  
4. FROM → GROUP BY → SELECT  

**6** What is the difference between WHERE and HAVING?

1. WHERE filters groups; HAVING filters individual rows  
2. HAVING filters groups; WHERE filters individual rows  
3. HAVING works only with aggregate functions; WHERE works with any expressions  
4. WHERE can filter by any column or expression; HAVING filters by values in SELECT or aggregates  
5. HAVING is always used after GROUP BY; WHERE can be used before or after GROUP BY  

**7** What does `SELECT COUNT(*)` return?

1. The number of rows in the table, excluding NULL values  
2. The number of rows where cells contain symbols  
3. The number of all rows in the table, including NULLs  
4. The sum of rows where cells contain symbols  

**8** The “Animals” table in a zoo database contains animals like: red fox, grey fox, little fox.  
Write a query that returns the age of the foxes.

1. `SELECT age FROM Animals WHERE Animal LIKE "%fox"`  
2. `SELECT age FROM %Fox.Animals`  
3. `SELECT age FROM Animals WHERE Animal = fox`  
4. `SELECT %fox age FROM Animals`  

**9** What is the difference between DELETE and TRUNCATE?

1. DELETE and TRUNCATE are the same  
2. DELETE removes one or more specific rows, TRUNCATE removes all rows  
3. DELETE can use a WHERE clause; TRUNCATE always deletes all records  
4. DELETE removes data; TRUNCATE deletes the table itself  

**10** Given the table:

```
COLOR
------
BLUE
RED
null
RED
```

What is the result of the query:  
`SELECT COUNT(DISTINCT color) FROM Table`

1. BLUE, RED, NULL  
2. 3  
3. 1, 2, 4  
4. 2  

---

## 2. Databases – ER Diagram

The database contains an `orders` table with the following fields:  
`id` (order ID), `name` (order name), `town` (delivery address), `price`, `customer_id`.  
There are also `towns`, `items`, and `customers` tables.  
There is a many-to-many relationship between `orders` and `items`.

**Task:**  
Design an ER diagram based on this input.  
You may define the remaining fields as you see fit, but include the given fields for the `orders` table.

---

## 3. Integrations

Imagine you are working as an analyst designing a shopping app.  
You need to model the following user journey:

- Display a product catalog (list of items with short descriptions)  
- Navigate from the catalog to a product detail page  
- Add a product to the shopping cart  

**Task:**  
Design the REST APIs needed for this scenario.  
Include the request and a sample JSON response for each endpoint.  
You may use any online store as a reference for the data model.

Additionally, build a **Sequence UML diagram** to illustrate this scenario.

---

## 4. Algorithmic Thinking

Let’s take a mobile banking app as an example.  
**Initial condition:** You have a smartphone with the app installed, but it is turned off.

**Task:**  
Using any notation, draw a diagram describing the full process of topping up your mobile phone balance with **€100** using the app.  
You can use any banking app you’re familiar with as a reference.
