# Database Normalization
Normalization is a technique for organizing data in a database. It is important that a database is normalized to minimize redundancy (duplicate data) and to ensure only related data is stored in each table. It also prevents any issues stemming from database modifications such as insertions, deletions, and updates.


# Normalization Stages
The stages of organization are called normal forms

## First Normal Form (1NF):

- Data is stored in tables with rows uniquely identified by a primary key (there must be primary key in a table)

- Data within each table is stored in individual columns in its most reduced form. for example , table has column called **contact_person_and_role**
can be divided into two columns such as contact_person and contact_role

- There are no repeating groups


## Second Normal Form (2NF):
- Everything from 1NF

- Only data that relates to a table’s primary key is stored in each table

## Third Normal Form (3NF):
- Everything from 2NF

- There are no in-table dependencies between the columns in each table


## What is a Primary Key?

A primary is a single column value used to identify a database record uniquely.

- It has the following attributes

- A primary key cannot be NULL

 - A primary key value must be unique

- The primary key values should rarely be changed

- The primary key must be given a value when a new record is inserted.


## What is a Foreign Key
Foreign Key references the primary key of another Table! It helps connect your Tables

- A foreign key can have a different name from its primary key

- It ensures rows in one table have corresponding rows in another

- Unlike the Primary key, they do not have to be unique. Most often they aren't

- Foreign keys can be null even though primary keys can not