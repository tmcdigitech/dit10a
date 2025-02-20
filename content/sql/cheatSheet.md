---
title: SQL cheat sheet
---
## Querying Data in SQL
### SELECT
Retrieve data from one or more tables
```sql
SELECT * FROM employees;
```

### DISTINCT
Select unique values from a column
```sql
SELECT DISTINCT department FROM
employees;
```

### WHERE
Filter rows based on specified conditions
```sql
SELECT * FROM employees WHERE
salary > 55000.00;
```

### LIMIT
Limit the number of rows returned in the
result set
```sql
SELECT * FROM employees LIMIT 3;
```

### FETCH
Retrieve a specified number of rows from
the result set
```sql
SELECT * FROM employees FETCH FIRST 3 ROWS ONLY;
```

## Filtering Data in SQL
### WHERE
Filter rows based on specified conditions
```sql
SELECT * FROM employees WHERE department = 'IT';
```

### LIKE
Match a pattern in a column
```sql
SELECT * FROM employees WHERE first_name LIKE 'J%';
```

### IN
Match any value in a list
```sql
SELECT * FROM employees WHERE department IN ('HR', 'Finance');
```

### BETWEEN
Match values within a specified range
```sql
SELECT * FROM employees WHERE salary BETWEEN 50000 AND 60000;
```

### IS NULL
Match NULL values
```sql
SELECT * FROM employees WHERE department IS NULL;
```

## SQL Operator
### AND
Combines multiple conditions in a WHERE clause
```sql
SELECT * FROM employees WHERE
department = 'IT' AND salary >
60000;
```

### OR
Specifies multiple conditions where any one
of them should be true
```sql
SELECT * FROM employees WHERE
department = 'HR' OR department =
'Finance';
```

### NOT
Negates A Condition
SELECT * FROM employees WHERE NOT
department = 'IT';
ORDER BY
Sorts the Result Set in Ascending or
Descending Order
SELECT * FROM employees ORDER BY
salary DESC;
GROUP BY
Groups Rows that have the Same Values into
Summary Rows
SELECT department, COUNT(*) AS
employee_count FROM employees GROUP
BY department;

## Aggregation Data in SQL
### COUNT
Count the number of rows in a result set
```sql
SELECT COUNT(*) FROM employees;
```

### SUM
Calculate the sum of values in a column
```sql
SELECT SUM(salary) FROM employees;
```

### AVG
Calculate the average value of a column
```sql
SELECT AVG(salary) FROM employees;
```

### MIN
Find the minimum value in a column
```sql
SELECT MIN(salary) FROM employees;
```

### MAX
Find the maximum value in a column
```sql
SELECT MAX(salary) FROM employees;
```
