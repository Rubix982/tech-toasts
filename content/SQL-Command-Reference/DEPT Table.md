---
title: "DEPT Table"
metaTitle: "Department Table DDL/DML"
metaDescription: "Department Table DDL/DML"
---

## DEPT (Department) Table

## Table Of Contents

- [DEPT (Department) Table](#dept-department-table)
- [Table Of Contents](#table-of-contents)
- [DDL](#ddl)
- [DML](#dml)

## DDL

The below SQL generates,

```sql
CREATE TABLE DEPT (
    DEPTNO INT(5) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    DNAME VARCHAR(20) NOT NULL,
    LOC VARCHAR(20) NOT NULL
);
```

Generates,

## DML

Insert data,

```sql
INSERT INTO DEPT(DEPTNO, DNAME, LOC) VALUES(10, "ACCOUNTING", "NEW YORK");
INSERT INTO DEPT(DEPTNO, DNAME, LOC) VALUES(20, "RESEARCH", "DALLAS");
INSERT INTO DEPT(DEPTNO, DNAME, LOC) VALUES(30, "SALES", "CHICAGO");
INSERT INTO DEPT(DEPTNO, DNAME, LOC) VALUES(40, "OPERATIONS", "BOSTON");
```
