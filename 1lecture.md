# SQL Datatypes
They define the type of values that can be stored in a column

## Signed and Unsigned
TINYINT UNSIGNED(0 to 255)
TINYINT(-128 to 127)

# Types of SQL Commands

DDL(Data Defintion Language): create, alter, rename, truncate & drop

DQL(Data Query Language): select

DML(Data Manipulation Language): insert, update & delete

DCL(Data Control Language): grant & revoke permission to users

TCL(Transaction Control Language): start transaction, commit, rollback

# Database related Queries

CREATE DATABASE db_name;
CREATE DATABASE IF NOT EXISTS db_name;

DROP DATABASE db_name;
DROP DATABASE IF EXISTS db_name;

SHOW DATABASES;

SHOW TABLES;


# Table related Queries
`Table name is case sensitive. Write table name in lower case generally.`
## 1. Create
Used to define table schema(design->columns)

CREATE TABLE table_name (
column_name1 datatype constraint,
column_name2 datatype constraint,
);

Example
CREATE TABLE student (
   rollno INT PRIMARY KEY,
   name VARCHAR(50)
);


## 2. Select & View ALL columns
SELECT * FROM table_name;

Example
SELECT * FROM student;

## 3. Insert
INSERT INTO table_name
(colname1, colname2)
VALUES
(col1_v1, col2_v1),
(col1_v2, col2_v2);

* Example
### For multiple values
INSERT INTO student
(rollno, name)
VALUES
(101, "karan"),
(102, "arjun");

### For single values
INSERT INTO student VALUES (104, "shyam");

