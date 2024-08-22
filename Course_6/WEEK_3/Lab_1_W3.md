# Hands-on Lab: Built-in Functions

In SQL, you can access many built-in functions that may be used to get more variety in our data analysis. These functions include aggregation functions (like MAX, MIN, SUM, and AVG), string functions (like LENGTH, UCASE, and LCASE), scalar functions (like ROUND), and a variety of date functions as well. In this tab, you'll get hands-on practice on how to use all of them.

## Software used

[MySQL](https://www.mysql.com/): MySQL is a Relational Database Management System (RDBMS) designed to store, manipulate, and retrieve data efficiently.

## User interface

[phpMyAdmin(]https://demo.phpmyadmin.net/master-config/public/)

![image](https://github.com/user-attachments/assets/d0370385-a3aa-4328-838d-739245674627)

### Create the example table

Use the script PETRESCUE-CREATE.sql:

```
drop table if exists PETRESCUE;

create table PETRESCUE (
	ID INTEGER NOT NULL,
	ANIMAL VARCHAR(20),
	QUANTITY INTEGER,
	COST DECIMAL(6,2),
	RESCUEDATE DATE,
	PRIMARY KEY (ID)
	);

insert into PETRESCUE values 
	(1,'Cat',9,450.09,'2018-05-29'),
	(2,'Dog',3,666.66,'2018-06-01'),
	(3,'Dog',1,100.00,'2018-06-04'),
	(4,'Parrot',2,50.00,'2018-06-04'),
	(5,'Dog',1,75.75,'2018-06-10'),
	(6,'Hamster',6,60.60,'2018-06-11'),
	(7,'Cat',1,44.44,'2018-06-11'),
	(8,'Goldfish',24,48.48,'2018-06-14'),
	(9,'Dog',2,222.22,'2018-06-15')
	
;

```
Resulting Table

![image](https://github.com/user-attachments/assets/7d273167-3096-4d54-a3ab-9d0906e54e3e)





### Aggregation Functions
1) Write a query that calculates the total cost of all animal rescues in the PETRESCUE table.
SELECT SUM(COST) FROM PETRESCUE;

2) You can further assign a label to the query SUM_OF_COST.
SELECT SUM(COST) AS SUM_OF_COST FROM PETRESCUE;

3) Write a query that displays the maximum quantity of animals rescued (of any kind).
For this query, we will use the function MAX(COLUMN_NAME). The output of this query will be the maximum value of all elements in the column. The query for this question can be written as:

SELECT MAX(QUANTITY) FROM PETRESCUE;

4) The query can easily be changed to display the minimum quantity using the MIN function instead.

SELECT MIN(QUANTITY) FROM PETRESCUE;

5) Write a query that displays the average cost of animals rescued.

SELECT AVG(COST) FROM PETRESCUE;


### Scalar Functions

1) Write a query that displays the rounded integral cost of each rescue.

For this query, we will use the function ROUND(COLUMN_NAME, NUMBER_OF_DECIMALS). The output of this query will be the value of each element in the column rounded to the specified number of decimal places. Note that the second argument is optional and, if omitted, results in rounding to an integer value. The query for this question can be written as:

SELECT ROUND(COST) FROM PETRESCUE;

 or

 SELECT ROUND(COST, 0) FROM PETRESCUE;

In case the question was to round the value to 2 decimal places, the query would change to:

SELECT ROUND(COST, 2) FROM PETRESCUE;

2) Write a query that displays the length of each animal name.
For this query, we will use the function LENGTH(COLUMN_NAME). The output of this query will be the length of each element in the column. The query for this question can be written as:

SELECT LENGTH(ANIMAL) FROM PETRESCUE;

3) Write a query that displays the animal name in each rescue in uppercase.

For this query, we will use the function UCASE(COLUMN_NAME). The output of this query will be each element in the column in upper case letters. The query for this question can be written as:

SELECT UCASE(ANIMAL) FROM PETRESCUE;

Just as easily, the user could ask for a lower case representation, and the query would be changed to:

SELECT LCASE(ANIMAL) FROM PETRESCUE;


### Date Functions 




