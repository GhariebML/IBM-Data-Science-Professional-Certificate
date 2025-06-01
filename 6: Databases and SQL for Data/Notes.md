# 📝 Notes – Databases and SQL for Data Science

These notes summarize the key concepts, commands, and use cases learned during Course 6 of the IBM Data Science Professional Certificate.

---

## 🔹 1. Introduction to Databases

- **Relational Database**: A collection of tables with relationships defined between them.
- **Table**: Consists of rows and columns; each column has a name and data type.
- Common DBMS: IBM Db2, MySQL, PostgreSQL, SQLite, Oracle.

---

## 🔹 2. Basic SQL Commands

### 🧾 Selecting Data
```sql
SELECT column1, column2
FROM table_name;
```

### 🧾 🧪 Filtering Data
```sql
SELECT * FROM table_name
WHERE column = 'value';
```

### 🧾 Logical Operators
```sql
-- AND / OR
SELECT * FROM table WHERE col1 = 'A' AND col2 > 10;

-- IN
SELECT * FROM table WHERE col IN ('A', 'B', 'C');

-- BETWEEN
SELECT * FROM table WHERE salary BETWEEN 30000 AND 60000;
```

## 🧾 3. Sorting, Limiting, Aliasing
```sql
-- ORDER BY
SELECT * FROM employees ORDER BY salary DESC;

-- LIMIT
SELECT * FROM employees LIMIT 5;

-- AS (alias)
SELECT name AS EmployeeName FROM employees;

```

## 🧾 4. Aggregate Functions
```sql
SELECT COUNT(*), AVG(salary), MAX(salary), MIN(salary)
FROM employees
WHERE department = 'IT';
```

## 🧾  5. Grouping and Filtering Groups
```sql
-- GROUP BY
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department;

-- HAVING
SELECT department, AVG(salary) 
FROM employees 
GROUP BY department
HAVING AVG(salary) > 50000;
```

## 🧾  6. Table Joins
```sql
-- INNER JOIN
SELECT *
FROM employees e
INNER JOIN departments d ON e.dept_id = d.id;

-- LEFT JOIN
SELECT *
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.id;
```

## 🧾  7. Subqueries
```sql
SELECT name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

### 🧾  8. Creating & Modifying Tables
```sql
-- CREATE
CREATE TABLE employees (
  id INT,
  name VARCHAR(50),
  salary FLOAT
);

-- INSERT
INSERT INTO employees (id, name, salary) VALUES (1, 'Ali', 50000);

-- UPDATE
UPDATE employees SET salary = 55000 WHERE id = 1;

-- DELETE
DELETE FROM employees WHERE id = 1;
```

### 🧾 9. Views
```sql
-- CREATE VIEW
CREATE VIEW high_earners AS
SELECT * FROM employees WHERE salary > 60000;

-- SELECT FROM VIEW
SELECT * FROM high_earners;
```


