# Database
Database is `collection of data` in a format that can be easily accessed(Digital)

A software application used to manage our DB is called DBMS`(Database Management System)`

# Types of Databases

1. Relational Databases(also called RDBMS)
* Data stored in tables
Example MYSQL, Oracle, Microsoft SQL Server, PostgreSQL
** We use SQL to work with relational DBMS

2. Non-relational(NoSQL)
Data is not stored in tables
Example: MongoDB

# What is SQL?
`Structured Query Language`

SQL is aprogramming language used to interact with relational databases.

It is used to perform CRUD operations: Create Read Update Delete

# Creating our First Database
Our first SQL Query

## for creation of database
CREATE DATABASE db_name;
Example:
CREATE DATABASE temp1;
create database temp2;


## for deletion of database
DROP DATABASE db_name;


# Creating our First Table
USE db_name;

CREATE TABLE table_name (
column_name1 datatype constraint,
column_name2 datatype constraint,
column_name3 datatype constraint,
);

Example:

USE college;

CREATE TABLE student (
id INT PRIMARY KEY,
name VARCHAR(50),
age INT NOT NULL
);

# Inserting values into table
INSERT INTO student VALUES(1, "SAHUL", 21)
INSERT INTO student VALUES(2, "SASWAT", 22)

SELECT * FROM student;







