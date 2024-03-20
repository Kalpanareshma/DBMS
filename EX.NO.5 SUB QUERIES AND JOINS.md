# EX.NO.6 SubQueries, Views and Joins 
### DATE
## AIM
### To use SubQueries, Views and Joins in SQL 
## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
```
 select ename from emp where sal>(select sal from emp where empno=7566);
```

### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/6d72287f-f1c5-4176-890f-cddebfcdc702)


### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
```
 select ename,job,sal from emp where sal = (select min(sal) from emp);
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/53461b03-340c-4dd5-a517-23c10080c764)


### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
```
> SELECT ename, job
-> FROM emp
-> WHERE deptno = 10 AND job IN (SELECT job FROM emp WHERE job = 'SALES');
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/c579e160-2b9e-4b13-ada1-e2acb75fa130)



### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
```
 CREATE VIEW emv5 AS SELECT empno, ename, job FROM emp WHERE deptno = 10;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/cdd31354-fe06-4406-94ee-53a554b220b7)


### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:
```
CREATE VIEW emv30 AS SELECT empno AS `Employee Number`, ename AS `Employee Name`, sal AS `Salary` FROM emp WHERE deptno = 30;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/05e5cdf4-3d5a-4f4d-bd32-094988fb957a)


### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
```
 UPDATE emv5 SET sal = sal * 1.1 WHERE job = 'CLERK';
 UPDATE emp
    -> SET sal = sal * 1.10
    -> WHERE job = 'CLERK';
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/07e2c56b-8196-4561-b2f9-ccd0b8e6dc01)
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/07b07451-3405-45af-92c7-988b74e7abd7)


## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
```
 SELECT salesman1.name AS "Salesman",
    ->        customer1.cust_name AS "Customer Name",
    ->        salesman1.city AS "City"
    -> FROM salesman1
    -> INNER JOIN customer1 ON salesman1.city = customer1.city;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/fd0954d3-43e7-4628-af2c-e5435cd46cae)


### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
```
 SELECT customer1.cust_name AS "Customer Name",
    ->        customer1.city AS "Customer City",
    ->        salesman1.name AS "Salesman",
    ->        salesman1.commission AS "Commission"
    -> FROM salesman1
    -> INNER JOIN customer1 ON salesman1.salesman_id = customer1.salesman_id
    -> WHERE salesman1.commission > 0.13;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/2a8fb401-6496-4218-b5d6-7e6b60e0a328)


### Q9) Perform Natural join on both tables

### QUERY:
```
 select * from Customer1 natural join salesman1;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/6efbc3ce-56ce-4391-9dcc-c9098ce20705)


### Q10) Perform Left and right join on both tables

### QUERY:
```
 SELECT *
    -> FROM salesman1
    -> LEFT JOIN customer1 ON salesman1.salesman_id = customer1.salesman_id;

 SELECT *
    -> FROM salesman1
    -> RIGHT JOIN customer1 ON salesman1.salesman_id = customer1.salesman_id;
```


### OUTPUT:
### LEFT JOIN:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/6c311f89-a040-4bc7-828f-1fa6ed2cf41d)
### RIGHT JOIN:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/f4c0f5d0-2a5c-479d-9c29-3b8f6352d8d6)



## RESULT 
### Thus the basics of subqueries,views,joins are performed in SQL.
