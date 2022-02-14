---
title: "SQL Joins & Operators"
metaTitle: "SQL Joins & Operators"
metaDescription: "SQL Joins & Operators"
---

## SQL JOIN

A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

## Table Of Contents

- [SQL JOIN](#sql-join)
- [Table Of Contents](#table-of-contents)
- [Different Types of SQL JOINs](#different-types-of-sql-joins)
- [SQL INNER JOIN Keyword](#sql-inner-join-keyword)
  - [INNER JOIN Syntax](#inner-join-syntax)
- [SQL LEFT JOIN Keyword](#sql-left-join-keyword)
- [SQL RIGHT JOIN Keyword](#sql-right-join-keyword)
- [Full Joins](#full-joins)

## Different Types of SQL JOINs

Here are the different types of the JOINs in SQL:

- (INNER) JOIN: Returns records that have matching values in both tables
- LEFT (OUTER) JOIN: Returns all records from the left table, and the matched records from the right table
- RIGHT (OUTER) JOIN: Returns all records from the right table, and the matched records from the left table
- FULL (OUTER) JOIN: Returns all records when there is a match in either left or right table

## [SQL INNER JOIN Keyword](https://www.w3schools.com/sql/sql_join_inner.asp)

The INNER JOIN keyword selects records that have matching values in both
tables.

### INNER JOIN Syntax

```sql
SELECT column_name(s)
  FROM table1
INNER JOIN table2
  ON table1.column_name = table2.column_name;
```

Example,

```sql
SELECT first_name, last_name, employees.department_id, departments.department_id,  department_name
  FROM employees
INNER JOIN
 departments ON departments.department_id = employees.department_id;
```

## [SQL LEFT JOIN Keyword](https://www.w3schools.com/sql/sql_join_inner.asp)

A LEFT JOIN statement returns all rows from the left table along with the rows from the right table for which the join condition is met

```sql
SELECT t1.emp_id, t1.emp_name, t1.hire_date, t2.dept_name
  FROM employees AS t1 LEFT JOIN departments AS t2
ON t1.dept_id = t2.dept_id ORDER BY emp_id;
```

## [SQL RIGHT JOIN Keyword](https://www.w3schools.com/sql/sql_join_inner.asp)

The RIGHT JOIN is the exact opposite of the [LEFT JOIN](https://www.tutorialrepublic.com/sql-tutorial/sql-left-join-operation.php).

It returns all rows from the right table along with the rows from the left table for which the join condition is met.

```sql
SELECT t1.emp_id, t1.emp_name, t1.hire_date, t2.dept_name
  FROM employees AS t1 RIGHT JOIN departments AS t2
ON t1.dept_id = t2.dept_id ORDER BY dept_name;                    
```

## Full Joins

A FULL JOIN returns all the rows from the joined tables, whether they are matched or not i.e. you can say a full join combines the functions of a [LEFT JOIN](https://www.tutorialrepublic.com/sql-tutorial/sql-left-join-operation.php) and a [RIGHT JOIN](https://www.tutorialrepublic.com/sql-tutorial/sql-right-join-operation.php).

Full join is a type of [outer join](https://www.tutorialrepublic.com/sql-tutorial/sql-joining-tables.php#outer-join)that's why it is also referred as *full outer join*.

```sql
SELECT t1.emp_id, t1.emp_name, t1.hire_date, t2.dept_name
  FROM employees AS t1 FULL JOIN departments AS t2
ON t1.dept_id = t2.dept_id ORDER BY emp_name;
```

The following example updates the stock table by increasing the unit_price value by 10% for a subset of prices. The WHERE clause specifies which prices to increase by applying the IN operator to the rows returned by a subquery that selects only the rows of the stock table where the unit_price value is less than 75.

```sql
UPDATE stock SET unit_price = unit_price * 1.1
  WHERE unit_price IN (
    SELECT unit_price FROM stock WHERE unit_price < 75
  );
```
