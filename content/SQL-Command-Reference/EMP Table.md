---
title: "EMP Table"
metaTitle: "Employee Table DDL/DML"
metaDescription: "Employee Table DDL/DML"
---

## EMP (Employee) Table

## Table Of Contents

- [EMP (Employee) Table](#emp-employee-table)
- [Table Of Contents](#table-of-contents)
- [DDL](#ddl)
- [DML](#dml)

## DDL

The below SQL generates,

```sql
CREATE TABLE EMP (
  EMPNO INT(5) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  ENAME VARCHAR(20) NOT NULL,
  JOB VARCHAR(20) NOT NULL,
  MGR INT(5) UNSIGNED,
  HIREDATE TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  SAL INT(5) UNSIGNED,
  COMM INT(5) DEFAULT NULL,
  DEPTNO INT(5)
);
```

Generates,

+----------+--------------+------+-----+-------------------+-----------------------------------------------+
| Field    | Type         | Null | Key | Default           | Extra                                         |
+----------+--------------+------+-----+-------------------+-----------------------------------------------+
| EMPNO    | int unsigned | NO   | PRI | NULL              | auto_increment                                |
| ENAME    | varchar(20)  | NO   |     | NULL              |                                               |
| JOB      | varchar(20)  | NO   |     | NULL              |                                               |
| MGR      | int unsigned | YES  |     | NULL              |                                               |
| HIREDATE | timestamp    | YES  |     | CURRENT_TIMESTAMP | DEFAULT_GENERATED on update CURRENT_TIMESTAMP |
| SAL      | int unsigned | YES  |     | NULL              |                                               |
| COMM     | int          | YES  |     | NULL              |                                               |
| DEPTNO   | int          | YES  |     | NULL              |                                               |
+----------+--------------+------+-----+-------------------+-----------------------------------------------+

## DML

Insert data,

```sql
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7369, "Smith", "CLERK", 7982, "2005-12-17", 800, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7499, "ALLEN", "SALESMAN", 7698, "2006-02-20", 1600, 300, 30);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7521, "WARD", "SALESMAN", 7698, "2006-02-22", 1250, 500, 30);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7566, "JONES", "MANAGER", 7839, "2006-04-02", 2975, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7654, "MARTIN", "SALESMAN", 7698, "2006-09-28", 1250, 1400, 30);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7698, "BLAKE", "MANAGER", 7839, "2006-04-02", 2975, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7782, "CLARK", "MANAGER", 7839, "2006-04-02", 2975, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7788, "SCOTT", "ANALYST", 7566, "2006-04-02", 2975, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, HIREDATE, SAL, DEPTNO) VALUES (7839, "KING", "PRESIDENT", "2006-11-17", 5000, 10);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO) VALUES (7844, "TURNER", "SALESMAN", 7698, "2006-09-08", 1500, 0, 30);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7876, "ADAMS", "CLERK", 7788, "2008-01-12", 1100, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7900, "JAMES", "CLERK", 7698, "2006-12-03", 950, 30);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7902, "FORD", "ANALYST", 7566, "2006-12-03", 3000, 20);
INSERT INTO EMP(EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, DEPTNO) VALUES (7934, "MILLER", "CLERK", 7782, "2006-01-23", 1300, 10);
```
