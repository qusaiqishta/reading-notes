# SQL

SQL, or Structured Query Language, is a language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database. And due to its simplicity, SQL databases provide safe and scalable storage for millions of websites and mobile applications. Example of SQL databases that uses SQL language standard are SQLite, MySQL, Postgres, Oracle and Microsoft SQL Server.

# Relational databases
A relational database represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

For example, if the Department of Motor Vehicles had a database, you might find a table containing all the known vehicles that people in the state are driving. This table might need to store the model name, type, number of wheels, and number of doors of each vehicle for example. In such a database, you might find additional related tables containing information such as a list of all registered drivers in the state, the types of driving licenses that can be granted, or even driving violations for each driver. With SQL you change , update and manipulate the relational database.
 
 ## SQl commands
 Here are some commands used by SQL to manipulate databases:

1-selsect
- To select specific columns use 

SELECT column, another_column, …
FROM mytable;

- to select all the table use 

SELECT * 
FROM mytable;

2-WHERE :In order to filter certain results from being returned
```
SELECT column, another_column, …

FROM mytable

WHERE condition

    AND/OR another_condition
    AND/OR …;
```

3- SELECT DISTINCT :DISTINCT keyword will blindly remove duplicate rows

```
SELECT DISTINCT column, another_column, …
FROM mytable
WHERE condition(s);
```

4- ORDER BY:o sort your results by a given column in ascending or descending order

```
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC;
```

5-LIMIT and OFFSET: The LIMIT will reduce the number of rows to return, and the optional OFFSET will specify where to begin counting the number rows from.

```
SELECT column, another_column, …
FROM mytable
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset;

```
# Database Normalization 
Database normalization is the process of structuring a database, usually a relational database, in accordance with a series of so-called normal forms in order to reduce data redundancy and improve data integrity.

### Multi-table queries with JOINs
combine row data across two separate tables using this unique key

1- Inner join:The INNER JOIN is a process that matches rows from the first table and the second table which have the same key (as defined by the ON constraint) to create a result row with the combined columns from both tables

```
SELECT column, another_table_column, …
FROM mytable
INNER JOIN another_table 
    ON mytable.id = another_table.id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

```
2-OUTER JOINs:If the two tables have asymmetric data, which can easily happen when data is entered in different stages, then we would have to use a LEFT JOIN, RIGHT JOIN or FULL JOIN instead to ensure that the data you need is not left out of the results. LEFT JOIN simply includes rows from A regardless of whether a matching row is found in B. The RIGHT JOIN is the same, but reversed, keeping rows in B regardless of whether a match is found in A. Finally, a FULL JOIN simply means that rows from both tables are kept, regardless of whether a matching row exists in the other table.


```
SELECT column, another_column, …
FROM mytable
INNER/LEFT/RIGHT/FULL JOIN another_table 
    ON mytable.id = another_table.matching_id
WHERE condition(s)
ORDER BY column, … ASC/DESC
LIMIT num_limit OFFSET num_offset;

```