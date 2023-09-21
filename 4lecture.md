# Joins in SQL
Venn Diagrams
Inner Join

Outer Join
Types
Left Join
Right Join
Full Join

`alias-->alternate name`
student as s
course as c

Oracle and PostgreSQL
FULL OUTER JOIN
FULL Join
works but not in MySQL

Think & Ans
## Left Exclusive Join
SELECT *
FROM student as a
LEFT JOIN course as b
ON a.id = b.id
WHERE b.id IS NULL;

## Right Exclusive Join
SELECT *
FROM student as a
RIGHT JOIN course as b
ON a.id = b.id
WHERE a.id IS NULL;

## Full Exclusive Join

# Self Join [PDF wrong screenshot]
## corrected part
SELECT a.name as manger_name, b.name
FROM employee as a
JOIN employee as b
ON a.id = b.manager_id;


# UNION

UNION
Doesnt allow duplicates
UNION ALL
Allows duplicates


# SQL Sub Queries
Involves 2 select statements
1. SELECT
2. FROM
3. WHERE(most preffered)

`Examples with WHERE`
## Example 1
SELECT AVG(marks) 
FROM student;

SELECT name, marks
FROM student
WHERE marks > 87.6667;

`For dynamic data, we use subquery`
1. SELECT name, marks
FROM student
WHERE marks > (SELECT AVG(marks) FROM student);

## Example 2
SELECT rollno
FROM student
WHERE rollno % 2 = 0;

SELECT name, rollno
FROM student
WHERE rollno IN (102, 104, 106);
`For dynamic data, we use subquery`
2. SELECT name, rollno
FROM student
WHERE rollno IN (
    SELECT rollno 
    FROM student 
    WHERE rollno % 2 = 0);


`Examples with FROM`
Whenever we use FROM, we have have to use alias to write the subquery

# using sub query
SELECT MAX(marks) 
FROM (SELECT * FROM student WHERE city = "Delhi") AS temp;

OR

# using normal query
SELECT MAX(marks)
FROM student
WHERE city = "Mumbai"

# MySQL Views
Virtual tables

CREATE VIEW view1 AS
SELECT rollno, name, marks FROM student;

SELECT * FROM view1;


