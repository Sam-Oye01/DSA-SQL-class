# PROJECT : Microsoft SQL Beginner class

**COURSE OUTLINES**

- Introduction to SQL 
- Introduction & Types of SQL Commands
- Introduction to SQL Queries
- SQL Tables
- SQL Clauses
- SQL operators
- SQL Views
- Introduction to Case When statement

## Day one(08 - 05 - 2025) 

### Introduction to SQL

FILE : [DSA-SQL For Data Analysis.pdf](https://github.com/user-attachments/files/20886169/DSA-SQL.For.Data.Analysis.pdf)

Today, we learnt the following

 -  What are Databases:  A database is an organized collection of data that 
is stored and managed in a structured way to allow 
for easy access, retrieval, and manipulation.
 -  What are the advantage of Databases : Data Integrity, Security, Backup and Recovery, Concurrency, Scalability, Efficient Data Management.
 -  How to use Database to Store Data.   
 -  Why Structured Query Language(SQL) or SEQUEL - Why Data Analyst use SQL :
     - SQL is easy to understand.
     - Traditional databases allow us to access data directly.
     - Traditional databases allow us to audit and replicate our data.
     - SQL is a great tool for analyzing multiple tables at once.
     - SQL allows you to analyze more complex questions than dashboard tools.
 -  Types of Databases (Microsoft Access, SQL Server, MySQL, PostgreSQL, Oracle, etc).
 -  SQL Operators and Clauses
     - SQL – Clause: where, order by, Group by, Having, Top.
     - SQL – Operators: Like, AND, OR, Between, Not Between, IN, NOT IN.
     - SQL - UNION Vs UNION ALL, INTERSECT.
     - SQL - Wild Card
     - SQL Joins
 -  SQL Aggregation
     - Introduction to SQL Aggregation
     - Introduction to Null
     - Aggregation: COUNT, SUM, AVERAGE, MIN, MAX etc
 -  SQL Views\
     - Introduction to SQL Views
     - SQL – Create views
     - SQL - update views
     - SQL – Drops
     - SQL – Rename views
 - SQL CASE WHEN STATEMENT
     - Introduction to CASE Statement
     - SQL – Create CASE WHEN Statement

## Day Two(12 - 05 -2025)

### Introduction & Types of SQL Commands

Today, we began practical sessions on SQL. WE treated the following;

 -  SQL Commands
     - Download and Install SQL Server 2022
     - Introduction to SQL Command
     - Types of SQL Commands : DDL, DML, DCL, DQL, and TCL
 - Writing SQL Queries
     - Introduction to SQL Queries ( Create first Database)
     - SQL - Data Types
     - SQL - Create table
     - SQL - Keys: Unique keys, Primary Keys, Foreign Keys.
     - SQL - Insert into Table, select Table
     - SQL - Drop, Delete, Truncate, Rename
     - SQL – Alter tables, Update tables, Drop tables, Delete tables, Truncate tables

It was an interesting class and we wrote the following queries
 
 ``` SQL ```

CREATE DATABASE DSA_db

-----Table creation-------

CREATE table Employees (Staff_id varchar (10),
First_Name varchar (100),
Last_Name Varchar (100),
Gender nvarchar (10),
Date_of_Birth date,
Hire_Date date,
primary key (staff_id)
)

Select * from Employees

------Insert-----------

Insert into Employees (Staff_id, First_Name, Last_Name, Gender, Date_of_Birth, Hire_Date)

values ( 'AB201', 'Ayan', 'Olakun', 'female', '1992-08-22', '2018-02-09')

Insert into Employees (Staff_id, First_Name, Last_Name, Gender, Date_of_Birth, Hire_Date)

values ( 'AB212', 'okorie', 'mercy', 'female','1988-10-09', '2018-10-09'),
( 'AB223', 'joshua', 'chukwuemeka', 'male','1980-10-09', '2022-02-09'),
( 'AB234', 'sanni', 'ibrahim', 'male','1958-10-09', '2019-09-23'),
( 'AB254', 'mercy', 'olanipekun', 'female','1982-10-09', '2020-02-09'),
( 'AB249', 'johnson', 'mercy', 'female','1982-10-09', '2019-12-09'),
( 'AB298', 'ayomide', 'halleluyah', 'female', '1982-10-09','2018-07-11'),
( 'AB260', 'deborah', 'justin', 'female','1982-10-09', '1988-02-09'),
( 'AB281', 'wale', 'olanipekun', 'male','1982-10-09', '2018-02-09')

Note: SQL is not case sensitive. Generally, keywords of SQL are written in uppercase. 
Secondly, The default database is the master database, you must change it before writing any query to the database that is needed. 

## Day Three(14 - 05 - 2025)

### Introduction to SQL Queries

Today, we moved forward with the hands-on training using Microsoft SQL server. We learnt the following;

 - SQL - Drop, Delete, Truncate, Rename
 - SQL - Alter tables, Update tables, Drop tables, Delete tables, Truncate tables

We wrote the following queries
 
 ``` SQL ```

 Drop Table Employees

-----Drop table Employees-----

-----IMPORT CSV FILES INTO DSA_db

---EMPLOYEE.CSV

---SALARY.CSV

---PAYMENT.CSV

 select * from Employee




## Day Four(15 - 05 -2025)

SQL Tables

## Day Five(19 - 05 - 2025)

SQL Clauses

## Day Six(21 - 05 - 2025)

SQL operators

## Day Seven(22 - 05 -2025)

SQL Views

## Day Eight(26 - 05 -2025) 

Introduction to Case When statement
