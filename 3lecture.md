## DISTINCT
Show unique values

SELECT DISTINCT city FROM student;

## WHERE Clause
SELECT *
FROM student
WHERE city = "Mumbai";

# Limit Clause

# Order By Clause
Ascending
Descending
By default, ascening order

# Aggregate Functions
COUNT()
MAX()
MIN()
SUM()
AVG()

SELECT MAX(marks) 
FROM student;

# Group By Clause


# Practice Qs

SELCT mode, count(customer)
FROM payment
GROUP BY mode;



## Having Clause
having clause is used for groups

SELECT city
FROM student
WHERE grade = "A"
GROUP BY city
HAVING MAX(marks) > 93
ORDER BY city DESC;

# Table related Queries
## 1. Update(to update existing rows)

SET keyword

UPDATE student
SET grade = "0"
WHERE grade = "A";

MySQL safe mode
To turn off safe mode
SET SQL_SAFE_UPDATES = 0;
To turn on safe mode
SET SQL_SAFE_UPDATES = 1;

UPDATE studnet
SET marks = marks + 1;

## 2. Delete(to delete existing rows)

DELETE FROM student
WHERE marks > 30;


# Revisiting FK(Foreign Keys)
CREATE TABLE dept (
   id INT PRIMARY KEY,
   name VARCHAR(50)
);

CREATE TABLE teacher (
   id INT PRIMARY KEY,
   name VARCHAR(50),
   dept_id INT,
   FOREIGN KEY (dept_id) REFERENCES dept(id)
);


parent tabele(dept)
child table(teacher)

# Cascading for FK
On Delete Cascade
On Update Cascade

CREATE TABLE teacher (
   id INT PRIMARY KEY,
   name VARCHAR(50),
   dept_id INT,
   FOREIGN KEY (dept_id) REFERENCES dept(id)
   ON UPDATE CASCADE
   ON DELETE CASCADE
);

# 3. ALTER(to change the schema)
1. ADD Column
ALTER TABLE student
ADD COLUMN age INT;

2. DROP Column

3. RENAME Column

4. CHANGE Column

5. MODIFY Column

# Truncate(to delete table's data)



# Practise Question[4.png]
1. ALTER TABLE student
CHANGE name full_name VARCHAR(50);

2. DELETE FROM student
WHERE marks < 80;

3. ALTER TABLE student
DROP COLUMN grade;






