---
title: "Retrieving Records"
metaTitle: "Retrieving Records"
metaDescription: "Retrieving Records"
---

## Retrieving Records

## Table Of Contents

- [Retrieving Records](#retrieving-records)
- [Table Of Contents](#table-of-contents)
- [Referencing An Aliased Column In The WHERE Clause](#referencing-an-aliased-column-in-the-where-clause)
  - [Problem](#problem)
  - [Solution](#solution)
  - [Discussion](#discussion)
- [Concatenating Column Values](#concatenating-column-values)
  - [Problem](#problem-1)
  - [Solution](#solution-1)
  - [Discussion](#discussion-1)
- [Using Conditional Logic In A SELECT Statement](#using-conditional-logic-in-a-select-statement)
  - [Problem](#problem-2)
  - [Solution](#solution-2)
  - [Discussion](#discussion-2)
- [Limiting The Number Of Rows Returned](#limiting-the-number-of-rows-returned)
  - [Problem](#problem-3)
  - [Solution](#solution-3)
  - [Discussion](#discussion-3)
- [Returning n Random Records From A Table](#returning-n-random-records-from-a-table)
  - [Problem](#problem-4)
  - [Solution](#solution-4)
  - [Discussion](#discussion-4)
- [Specifying Null Values](#specifying-null-values)
  - [Problem](#problem-5)
  - [Solution](#solution-5)

## Referencing An Aliased Column In The WHERE Clause

### Problem

You hav used aliases to provide more meaningful column names for your result set and would like to exclude some of the rows using the WHERE clause.

However, your attempt to reference alias names in the WHERE clause fails:

```sql
select sal as salary, comm as commission
    from emp
where salary < 5000;
```

### Solution

By wrapping your query as an inline view, you can reference the aliased columns,

```sql
select *
    from (
    select sal as salary, comm as commission
    from emp        
    ) x
where salary < 5000;
```

### Discussion

This is what you need to do when attempting to reference any of the following in a WHERE clause,

- Aggregate functions
- Scalar subqueries
- Windowing functions
- Aliases

## Concatenating Column Values

### Problem

You want to return values in a multiple columns as one column.

For example, you would like to produce,

```markdown
CLARK WORKS AS A MANAGER
KING WORKS AS A PRESIDENT
MILLER WORKS AS A CLERK
```

However, both data come from two different column, `ENAME` and `JOB` in the `EMP` TABLE,

```sql
select ename, job
    from emp
    where deptno = 10;
```

### Solution

Use the CONCAT function,

```sql
select concat(ename, ' WORKS AS A ', job) as msg
    from  emp
where deptno = 10;
```

### Discussion

For different databases:

- DB2/Oracle/PostgreSQL: Use `||`
- MySQL: Use `CONCAT`
- SQLServer: Use `+`

## Using Conditional Logic In A SELECT Statement

### Problem

You want to perform IF-ELSE operations on values in your SELECT statement.

For example,

- If employee is paid $2,000 or less, then "UNDERPAID"
- If employee is paid $4,000 or more, then "OVERPAID"
- Else "OK"

### Solution

Use the CASE expression to perform conditional logic directly in your SELECT statement,

```sql
select ename, sal,
    case when sal <= 2000 then 'UNDERPAID'
        case when sal >= 4000 then 'OVERPAID'
        else 'OK'
    end as status
from emp
```

### Discussion

Omit the ELSE, and the CASE expression will return NULL for any row that does not satisfy the test condition

You can also set alias for the output

## Limiting The Number Of Rows Returned

### Problem

You want to limit the number of rows returned in your query. You are not concerned with order; any n rows will do.

### Solution

Do the same thing in MySQL and PostgreSQL using LIMIT,

```sql
select *
    from emp limit 5;
```

### Discussion

Many vendors provide clauses such as `FETCH FIRST` and `LIMIT` that let you specify the number of rows to be returned from a query.

Oracle uses ROWNUM, for example,

```sql
select *
    from emp
where rownum <= 5;
```

## Returning n Random Records From A Table

### Problem

Successive retrieval executions will produce different sets of five rows,

```sql
select ename, job
    from emp;
```

### Solution

For each Database,

- MySQL,

```sql
select enam, job
    from emp
order by rand() limit 5;
```

### Discussion

These solution(s) all restrict the number of rows to return after the function in the ORDER BY clause is executed.

When specifying a numeric constant in the ORDER BY clause, you are requesting that the sort be done according the column in that ordinal `position` in the SELECT list.

## Specifying Null Values

### Problem

Find all rows that ar null for a particular column

### Solution

```sql

```
