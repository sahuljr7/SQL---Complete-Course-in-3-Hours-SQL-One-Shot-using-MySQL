# Keys
## 1. Primary Key
It is a column (or set of columns) in a table that uniquely identifies each row. (a unique id)
There is only 1 PK & it should be NOT null.

## 2. Foreign Key
A foreign key is a column (or set of columns) in a table that refers to the primary key in another table.
There can be multiple FKs.
FKs can have duplicate & null values.

# Constraints
SQL constraints are used to specify rules for data in a table.

## 1. NOT NULL
columns cannot have a null value
`col1 int NOT NULL`

## 2. UNIQUE
all values in column are different
`col2 int UNIQUE`

## 3. PRIMARY KEY
makes a column unique & not null but used only for one

`id INT PRIMARY KEY`

CREATE TABLE temp (
id int not null,
PRIMARY KEY (id)
);

# 2nd syntax for making primary key
CREATE TABLE temp1 (
id INT,
name VARCHAR(50),
age INT,
city VARCHAR(20),
PRIMARY KEY (id, name)
);
`We can make the combination of two columns as a primary key`


## 4. FOREIGN KEY 
prevent actions that would destroy links between tables

CREATE TABLE temp (
cust_id int,
FOREIGN KEY (cust_id) references customer(id)
);

## 5. DEFAULT 
sets the default value of a column

`salary INT DEFAULT 25000`

* Example

CREATE TABLE emp (
id INT,
salary INT DEFAULT 25000);

INSERT INTO emp (id) VALUES (101);

SELECT * FROM emp;

## 6. CHECK
