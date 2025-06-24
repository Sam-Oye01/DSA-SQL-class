# PROJECT : Microsoft SQL Beginner class

### COURSE OUTLINES

### Introduction to SQL 
### Introduction & Types of SQL Commands
### Introduction to SQL Queries
### SQL Tables
### SQL Clauses
### SQL Operators
### SQL Views
### Introduction to Case-When statement

## Day one(08 - 05 - 2025) 

### Introduction to SQL

FILE : [DSA-SQL For Data Analysis.pdf](https://github.com/user-attachments/files/20886169/DSA-SQL.For.Data.Analysis.pdf)

Today, we learnt the following;

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

## Day Two(12 - 05 -2025)

### Introduction & Types of SQL Commands

Today, we began practical sessions on SQL. WE treated the following;

 -  SQL Commands
     - Download and Install SQL Server 2022
     - Introduction to SQL Command
     - Types of SQL Commands : DDL, DML, DCL, DQL, and TCL
 - Writing SQL Queries
     - Introduction to SQL Queries ( Create Database first)
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

**Note**: SQL is not case sensitive. Generally, keywords of SQL are written in uppercase. 
Secondly, The default database is the master database, you must change it before writing any query to the database that is needed. 

## Day Three(14 - 05 - 2025)

### Introduction to SQL Queries

Today, we moved forward with the hands-on training using Microsoft SQL server. We learnt the following;

 - SQL - Drop, Delete, Truncate, Rename
 - SQL - Alter tables, Update tables, Drop tables, Delete tables, Truncate tables

-----IMPORT CSV FILES INTO DSA_db

---EMPLOYEE.CSV [Download here](https://github.com/user-attachments/files/20887214/Employee.csv)

---SALARY.CSV [Download here](https://github.com/user-attachments/files/20887265/salary.csv)

---PAYMENT.CSV [Download here](https://github.com/user-attachments/files/20887295/Payment.csv)

We wrote the following queries;
 
 ``` SQL ```

----CREATE Table Salary----  

	CREATE Table Salary (salary_id int identity (1,1)not null,
	Staffid varchar (255),
	firstname varchar (255),
	lastname varchar (255),
	department nvarchar(max),
	salary decimal (10, 3) ---(10: precision, 3:scale)
	)

	select * from Salary

	Insert into Salary (staffid, firstname, lastname, department, salary)
	values ( 'AB401', 'ayan', 'olakun', 'Information Tech.', 45000.45),
	( 'AB212', 'okorie', 'mercy','Account',500000.99999),
	( 'AB223', 'joshua', 'chukwuemeka', 'Human Resources',100560.9339999),
	( 'AB234', 'sanni', 'ibrahim', 'Sales and Marketing',845688.99),
	( 'AB254', 'mercy', 'olanipekun', 'Account',8889.999999),
	( 'AB249', 'johnson', 'mercy', 'Information Tech.',234000.90909090),
	( 'AB298', 'ayomide', 'halleluyah', 'Logistics', 678000.991999),
	( 'AB260', 'deborah', 'justin', 'Logistics',900099.00697969),
	( 'AB281', 'wale', 'olanipekun', 'Information Tech',873093.2344)
	
	select * from salary
	
 	Drop Table salary


-----CREATE TABLE PAYMENT-----

	CREATE TABLE PAYMENT (paymentid int identity (1,1) primary key,
	Account_No bigint not null,
	staffid int,
	Bank varchar (255) default 'Zenith Bank',
	Payment_Method varchar (50) check (Payment_Method = 'Cash' or Payment_Method = 'Transfer')
	)

	select * from PAYMENT

	insert into Payment (account_no, staffid, payment_method)
	values (2033030303, 'AB200', 'transfer'),
	(2123459910, 'AB401',  'transfer'),
	(2034562240, 'AB254',  'cash'),
	(2234556303, 'AB212',  'transfer'),
	(2033037703, 'AB249',  'cash'),
	(2033030303, 'AB298',  'cash'),
	(2455657503, 'AB260',  'transfer'),
	(2045595953, 'AB281',  'cash'),
	(2033030303, 'AB273',  'transfer'),
	(2077778903, 'AB299',  'transfer'),
	(2033030301, 'AB286', 'transfer'),
	(2123459911, 'AB260',  'transfer'),
	(2034562241, 'AB270',  'cash'),
	(2234556302, 'AB104',  'transfer'),
	(2033037705, 'AB268',  'cash'),
	(2033030306, 'AB270',  'cash'),
	(2455657509, 'AB300',  'transfer')

	insert into Payment
	values (2198773830, 'AB299',  'GT bank', 'transfer'),
	(2024656569, 'AB405',  'Access bank', 'cash'),
	(2222444933, 'AB200',  'Fidelity bank', 'transfer'),
	(5674842300, 'AB278', 'Access bank', 'transfer'),
	(2222444933, 'AB200',  'GT bank', 'transfer'),
	(2034537300, 'AB278', 'Access bank', 'transfer')

	alter table payment
	alter column staffid varchar (50)
	
	select * from PAYMENT

**Note**: Before importing files, you must ascertain the data source, know where it is stored and determine the data quality. Ensure you check the data types of the columns and confirm if it does not need to be changed. Also, you must specify primary key before importing files.

## Day Four(15 - 05 -2025)

### SQL Tables

Today, we took a step further on our SQL journey as we continued by exploring other SQL commands. We wrote the following queries;
 
 ``` SQL ```

----Use of SQL commands-----

----Update

	Update Employee
	set Last_Name = 'Abubakar'
	where Staff_Id = 'AB234'
	
	Select * from Employee
	
	Update salary
	set department = 'Information Tech'
	where Staffid = 'AB223'
	
	Select * from salary

-----Create State of Origin

----Alter

	Alter Table Employee
	Add [State of Origin] varchar (100)
	
	Update Employee
	set [State of Origin] = 'Rivers'
	where Staff_Id = 'AB405'
	
	Select * from Employee

-----Analysis----

-----Total no of staff

	Select count(distinct Staff_Id) as TotalEmployee
	from Employee

-----Calculate the total no of staffs from each states

	Select [state of Origin], count(distinct Staff_Id) as TotalEmployee
	from Employee
	group by [state of Origin]
	Order by TotalEmployee Asc

-----Calculate the total no of staffs from each department

	Select [department], count(distinct Staffid) AS TotalEmployee
	from salary
	group by [department]
	order by [department] asc
	
	Update salary
	set [department] = 'Information Tech'
	where Staffid In ('AB401', 'AB249')

-----Having

	Select [department], count(distinct Staffid) as TotalEmployee
	from salary
	group by [department]
	Having count(distinct Staffid) >= 3

-------RELATIONAL OPERATORS/COMPARISON OPERATORS

----LESS THAN <

----GREATER THAN >

	Select * from salary 
	where salary < 500000
	
	Select * from salary 
	where salary > 500000

-----LOGICAL OPERATORS

----RANGE OPERATORS

----BETWEEN

-----NOT BETWEEN

	Select * from salary 
	where salary BETWEEN 50000 AND 200000
	
	Select * from salary 
	where salary NOT BETWEEN 50000 AND 1000000


**Note:** We use box parenthesis [] when we want to introduce spaces in between our column names.

## Day Five(19 - 05 - 2025)

### SQL Clauses

Today we treated the following;

 -  SQL Operators and Clauses
     - SQL – Clause: where, order by, Group by, Having, Top.
     - SQL – Operators: Like, AND, OR, Between, Not Between, IN, NOT IN.
     - SQL - UNION Vs UNION ALL, INTERSECT.
     - SQL - Wild Card
     - SQL Joins
  
We wrote the following queries;

``` SQL ```

-----LIST OPERATORS----

-----IN

-----NOT IN

	SELECT * FROM Employee
	WHERE Staff_Id IN ('AB270', 'AB286', 'AB401')
	
	SELECT * FROM Employee
	WHERE First_Name NOT IN ('johnson', 'mercy', 'okorie')

----LOGICAL OPERATORS---

---AND - It is true once all the conditions are true, and false if otherwise. All conditions must be met for it to be true. All conditions are merged together to bring a result

---OR - It is true as long as one condition is met. All conditions do not need to be satisfied for it to be true. All conditions are treated singly to bring a result.

	SELECT * FROM Employee
	WHERE First_Name = 'ADEBOWALE' AND Gender = 'MALE'
	
	SELECT * FROM Employee
	WHERE First_Name = 'ADEBOWALE' OR Gender = 'FEMALE'

-----UPDATE

	UPDATE salary
	SET StafFID = 'AB350'
	WHERE StaffID = 'AB401'
	
	SELECT * from SALARY

-----5% or 0.05

	UPDATE salary
	SET salary = salary + (salary * '0.05')

-----SQL JOIN

----FULL JOIN

---INNER JOIN

---LEFT JOIN

---RIGHT JOIN

	SELECT Employee.Staff_Id,
	Employee.First_Name,
	Employee.Gender,
	Employee.Hire_Date,
	salary.salary_id,
	salary.department,
	salary.salary
	from Employee full outer join salary
	on Employee.Staff_Id = salary.Staffid

	SELECT * from Employee join salary
	on Employee.Staff_Id = salary.Staffid

	SELECT salary.salary_id,
	payment.paymentid,
	Employee.Staff_Id,
	Employee.First_Name,
	Employee.Gender,
	Employee.Hire_Date,
	salary.department,
	salary.salary,
	payment.Account_No,
	payment.Bank,
	payment.Payment_Method
	from Employee join salary
	on Employee.Staff_Id = salary.Staffid
	join payment
	on payment.staffid = salary.Staffid

**Note**: Ensure to use the primary key of the tables to connect them together, and know that the primary key is a unique identifier of every table. It becomes a foreign key in other tables. "Join" is synonymous to "Merge" in Power BI. Join works on the column of a table but set operations such as "Union" works on the rows.

## Day Six(21 - 05 - 2025)

### SQL operators

Today, the journey on coding using SQL continues. We treated Subqueries and SQL aggregation commands.

 -  SQL Aggregation
     - Introduction to SQL Aggregation
     - Introduction to Null
     - Aggregation: COUNT, SUM, AVERAGE, MIN, MAX etc

We wrote the following queries;

``` SQL ```

------Sub-queries : Queries within queries

---Using sub-queries to join tables

	SELECT * from (select Staff_id, First_Name, Last_Name, Gender, Date_of_Birth, Hire_Date, [State of Origin]
			from Employee) as Emp
	join (
	  select staffid, department, salary
				from salary) as Sal
	on emp.Staff_Id = sal.staffid

-----Analysis

-----top 3 highest paid employee

	SELECT top 3 * from (
			select staffid, firstname, lastname, department, salary
				from salary) as sal
	Order by Salary desc
	
	SELECT top 3
	Employee.Staff_Id,
	Employee.First_Name,
	Employee.Last_Name
	from Employee
	order by Staff_Id desc
	
	SELECT top 3 staffid, firstname, lastname, department, salary
				from salary
	Order by Salary desc

-----Average salary by department

	SELECT department, AVG(salary) AS [Average Salary] 
		from (
		select department, salary from salary) as [Dept salary]
	group by department

---or (the normal way)

	SELECT department, AVG(salary) AS [Average Salary] 
		from salary
	group by department

-----Get second highest paid employee---

	SELECT MAX(salary) as [second highest salary]
	from salary
	where salary < (SELECT MAX(salary) as [second highest salary]
	from salary)
	
	SELECT top 1 staffid, firstname, lastname, department, salary
				from salary
	where salary < (Select MAX(salary) as [second highest salary]
	from salary)
	order by salary desc;

--=-Get list of highest paid employee from the second highest----

	SELECT staffid, firstname, lastname, department, salary
				from salary
	where salary < (Select MAX(salary) as [second highest salary]
	from salary)
	order by salary desc;

----SQL view-----

	Create view [vw emplysal table]
	as
	SELECT Employee.Staff_Id,
	Employee.First_Name,
	Employee.Gender,
	Employee.Hire_Date,
	salary.salary_id,
	salary.department,
	salary.salary
	from Employee full outer join salary
	on Employee.Staff_Id = salary.Staffid
	select * from [vw emplysal table]
	
	drop view [vw emplysal table]

**Note**: A view is a Hypothetically generated that is a product of an originally stored table/the result of an SQL query.

## Day Seven(22 - 05 -2025)

### SQL Views

Today, it was another breathtaking session on SQL as we dived further into creating views and using SET operations.

 -  SQL Views
     - SQL – Create views
     - SQL - update views
     - SQL – Drops
     - SQL – Rename views

We wrote the following queries;

``` SQL ```

-----IMPORT CSV FILES INTO DSA_db

---DSA Mall Ikeja [Download here](https://github.com/user-attachments/files/20889212/Mall_Ikeja.csv)

---DSA Mall Portharcourt [Download here](https://github.com/user-attachments/files/20889224/Mall_Lekki.csv)

---DSA Mall Ghana [Download here](https://github.com/user-attachments/files/20889234/Mall_Marina.csv)


----SQL SET OPERATIONS

---UNION

---UNION ALL

	CREATE TABLE [DSA MALL IKEJA 2] (CustomerID INT not null,
	FirstName varchar (max),
	LastName varchar (max),
	[Customer gender] nvarchar (max),
	[Transaction Date] DATE DEFAULT GETDATE(),
	[Address] varchar (max),
	[Transaction Amount] decimal (18, 4)
	)
	
	select * from [DSA MALL IKEJA 2]
	
	ALter TABLE [DSA MALL IKEJA]
	ALter column FirstNamae varchar (max) 
	 
	insert into [DSA MALL IKEJA 2] (customerID,FirstName, lastName, [Customer gender],[Address], [Transaction amount])
	values ( 200,'Femk', 'abdukl',  'male', '9 old road', 88000.00),
	   (201, 'isaiah', 'john','male',  '22 alaly stree, okun', 1590.33),
	    ( 206,'emma', 'abu','male',  '7 ababa street, makunn', 6788.33),
		 (210, 'kara', 'ogun','female' , '10 hahroh road, ottawa', 3400.33),
		  ( 211,'sunkanmi', 'osagie', 'female' , '9 agric butstop street, okun', 89875.00),
		   (209,'oge', 'kunle', 'male', '10 iwo street, liverpool', 7860.33),
		    (204, 'igbayin', 'elizabeth', 'female', '100 kukuma street, epe', 89100.69)
     
-----Union

	select * from [DSA Mall Ikeja]
	union
	select * from [DSA Mall Ghana]
	union
	select * from [DSA Mall Portharcourt]
	order by CustomerID desc;

-----Union all

	select * from [DSA Mall Ikeja]
	union all
	select * from [DSA Mall Ghana]
	union all
	select * from [DSA Mall Portharcourt]
	order by CustomerID desc;

-----create column (Branch)------ 

	Create view [vw DSA MALL TRANSACTIONS]
	as
	SELECT 
	'[DSA Mall Ikeja]' as branch, CustomerID as [Customer ID],
	firstname as [First Name], lastname as [Last Name], customer_gender as Gender, Transactiondate as [Transaction Date],
	[Address], transaction_amount as [Transaction Amount] 
	from [DSA Mall Ikeja]
	union
	SELECT 
	'[DSA Mall Ghana]' as branch, CustomerID as [Customer ID],
	firstname as [First Name], lastname as [Last Name], customer_gender as Gender, Transactiondate as [Transaction Date],
	[Address], transaction_amount as [Transaction Amount] 
	from [DSA Mall Ghana]
	union
	SELECT 
	'[DSA Mall Portharcourt]' as branch, CustomerID as [Customer ID],
	firstname as [First Name], lastname as [Last Name], customer_gender as Gender, Transactiondate as [Transaction Date],
	[Address], transaction_amount as [Transaction Amount] 
	from [DSA Mall Portharcourt]

-----TOTAL SALES PER BRANCH

	SELECT branch, sum([Transaction Amount]) as  [total sales]
		from [vw DSA MALL TRANSACTIONS]
	 group by branch
	 order by [total sales] desc;

-----TOTAL SALES by gender

	SELECT Gender, sum([Transaction Amount]) as  [total sales]
		from [vw DSA MALL TRANSACTIONS]
	 group by Gender
	 order by [total sales] desc;

-----DOES CHANGES IN TABLES AFFECT VIEW? Yes.

	ALTER TABLE [DSA MALL IKEJA]
	ALTER COLUMN TransactionDate date default getdate()
	
	insert into [DSA MALL IKEJA] (customerID,FirstName, lastName, [Customer_gender], TransactionDate, [Address], [Transaction_amount])
	values ( 500,'Femk', 'abdukl',  'male','2025-05-27', '9 old road', 88000.00),
	   (501, 'isaiah', 'john','male', '2025-05-27', '22 alaly stree, okun',  1590.33),
	    ( 506,'emma', 'abu','male', '2025-05-27', '7 ababa street, makunn',  6788.33),
		 (510, 'kara', 'ogun','female' , '2025-05-27','10 hahroh road, ottawa',  3400.33),
		  ( 511,'sunkanmi', 'osagie', 'female' ,'2025-05-27', '9 agric butstop street, okun',  89875.00),
		   (509,'oge', 'kunle', 'male','2025-05-27', '10 iwo street, liverpool',  7860.33),
		    (504, 'igbayin', 'elizabeth', 'female','2025-05-27', '100 kukuma street, epe',  89100.69)
	
	select * from [DSA Mall Ikeja]
	
	select * from [vw DSA MALL TRANSACTIONS]


-----Date Analysis

	SELECT * from [vw DSA MALL TRANSACTIONS]
	where [Transaction Date] = '2025-05-27'
	
	SELECT Gender, sum([Transaction Amount]) as [total sales]
	from [vw DSA MALL TRANSACTIONS]
	where [Transaction Date] = '2025-05-27'
	group by gender 

------Analysis base branch (Ghana)

	select branch, sum([Transaction Amount]) as Revenue
	from [vw DSA MALL TRANSACTIONS]
	where branch = '[DSA Mall Ghana]'
	group by branch

----add gender----

	select gender, branch, sum([Transaction Amount]) as Revenue
	from [vw DSA MALL TRANSACTIONS]
	where branch = '[DSA Mall Ghana]'
	group by branch, Gender

-----add gender and date----

	select gender, branch, sum([Transaction Amount]) as Revenue
	from [vw DSA MALL TRANSACTIONS]
	where branch = '[DSA Mall Ikeja]' and [Transaction Date] = '2025-05-27'
	group by branch, Gender
	
	select gender, branch, sum([Transaction Amount]) as Revenue
	from [vw DSA MALL TRANSACTIONS]
	where branch = '[DSA Mall Ikeja]'
	group by branch, Gender

**Note**: In the "Union" operation, all the number of the data types and columns must be the same in both tables on which the union operation is to be applied. "Union" removes the duplicates rows while "Union all" Leaves them. 

## Day Eight(26 - 05 -2025) 

### Introduction to Case When statement

Finally, we get to the last class. The journey so far has not been easy honsetly but it was worth the stress. Today, we treated conditional queries on SQL.

 - SQL CASE WHEN STATEMENT
     - Introduction to CASE Statement
     - SQL – Create CASE WHEN Statement
  
-----CASE WHEN STATEMENTS

	Alter Table Employee
	Add [State of Origin] varchar (100)

	Alter Table Employee
	Alter column [State of Origin] varchar (255)

----Update state of origin---

-----Using where

	Update Employee
	set [State of Origin] = 'Lagos'
	where Staff_Id In ('AB401', 'AB249', 'AB212')

-----Using CASE WHEN

	Update Employee
	set [State of Origin] = 
 	CASE
    	when Staff_Id = 'AB200' THEN 'Delta'
   	when Staff_Id = 'AB212' THEN 'Lagos'
    	when Staff_Id = 'AB223' THEN 'Oyo'
	when Staff_Id = 'AB234' THEN 'Bauchi'
	when Staff_Id = 'AB240' THEN 'Port Harcourt'
	when Staff_Id = 'AB249' THEN 'Lagos'
 	when Staff_Id = 'AB254' THEN 'Edo'
   	when Staff_Id = 'AB260' THEN 'Ekiti'
   	when Staff_Id = 'AB268' THEN 'Delta'
   	when Staff_Id = 'AB270' THEN 'Lagos'
   	when Staff_Id = 'AB278' THEN 'Kano'
   	when Staff_Id = 'AB281' THEN 'kano'
   	when Staff_Id = 'AB282' THEN 'Ekiti'
   	when Staff_Id = 'AB286' THEN 'Lagos'
   	when Staff_Id = 'AB298' THEN 'Delta'
   	when Staff_Id = 'AB299' THEN 'Edo'
   	when Staff_Id = 'AB401' THEN 'Oyo'
   	when Staff_Id = 'AB405' THEN 'Delta'

	ELSE 'Unknown'
	END

	SELECT * FROM Employee
	WHERE [State of Origin] = 'Lagos'

	SELECT [state of origin], count([state of origin]) as [State numbers] from Employee
	Group by [state of origin] 
	Order by [State numbers] desc;

----Get staff age at commencement of Hire---

	ALter TABLE EMPLOYEE
 	ALter column Hire_date Date

	select * from Employee
	ALTER TABLE EMPLOYEE
	ADD Age AS DATEDIFF(Year, Date_of_Birth, Hire_Date) -
	CASE
      WHEN MONTH(Hire_Date) < MONTH(Date_of_Birth) 
	  OR (MONTH(Hire_date) = MONTH(Date_of_Birth) 
	  AND DAY(Hire_date) < DAY(Date_of_Birth))
	THEN 1
  	ELSE 0
	END

----Get staff age today

	ALter TABLE EMPLOYEE
	drop column Age

	ALTER TABLE EMPLOYEE
	ADD Age AS DATEDIFF(Year, Date_of_Birth, GETDATE()) -
 	CASE
	WHEN MONTH(Date_of_Birth) < GETDATE() 
	  OR (MONTH(Date_of_Birth) = GETDATE() 
	  AND DAY(Date_of_Birth) < GETDATE())
	THEN 1
 	ELSE 0
	END

	select * from Employee

-- 50 and above = Executive Director
---36 - 49 = Senior Manager
--26 and 35 = Manager
--less than 25 =  Assistant Manager

	create view Vw_EMPLOYEES_AGE_GROUP
	AS
	select Staff_Id, First_Name, Gender, [state of origin], Age,
  	CASE
  	 when Age  >= 50 then 'Executive Director'
	   when Age between 36 and 49 then 'Senior Manager'
	   when Age between 26 and 35 then 'Manager'
	   when Age <= 25 then 'Executive Trainee'
	 Else 'Unknown'
	End as [Age Group]
	from Employee

------File Back-up and Restore----

---Advantages

--1. For Data Protection for security purposes.

--2. For Data Recovery in the event of disaster or system failure.
