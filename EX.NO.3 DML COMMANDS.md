# EX 3 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/08b3adb1-4eaf-4f81-809f-85c2bbe09858)

### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ba2b28e8-c07f-4bd2-92a5-c7f9ff5cbcbb)


### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/2d04b041-76d9-42c8-b53b-09bf9b84f790)

### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/d457ebd6-dda6-4c5a-a815-0309fecffc7a)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/d7a19291-a819-4924-a76b-50e57d0e60e5)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/e36c7577-284c-48b9-9f5a-ceb8a28b31ef)


### Q5)	List the names of Clerks from emp table.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/c9d6cb7f-f046-468f-ba12-f07d5627656c)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/5690c103-3614-4b56-995c-8aa91fdf0632)



### Q6)	List the names of employee who are not Managers.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ed2b8bc6-9744-4507-9efa-6ee619b0121a)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ad292e85-71f6-4973-89e6-b552068d6238)



### Q7)	List the names of employees not eligible for commission.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/5fc05982-2582-4555-988e-68f98cfbedd5)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/17b71fea-e260-4aae-be9c-44f9af0f63bf)


### Q8)	List employees whose name either start or end with ‘s’.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/16563f38-79bb-4d5e-85d1-c3d5b3337913)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/1dc857c4-be2d-49af-9d8e-51033f6f6438)



### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/3b46d71d-8dc1-4ff5-945e-90edab99fd08)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/8432ddde-ac46-44e8-b704-670b2007c15f)



### Q10) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/09067236-5cb6-445d-a89a-e45e30b76c0c)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ab5fa265-34fc-4c77-9dfd-e3877f58f825)



### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/cda143f4-74ae-4505-8bf8-420e67dff1a9)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/6d5bb7f4-88f4-4cc7-99ad-9f16adb6052a)



### Q12) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/5fe92e25-66c7-4041-a034-0e916ebc2145)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/4be115c8-0a37-4565-8cc3-6b686cb5c809)


### Q13) Find number of rows in the table EMP

### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/e08f0ffb-7473-4863-a3a7-d04dbf49002f)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/8720bb8d-f4ca-41ef-b287-6fe267c30f09)



### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/26b1ef0f-e505-4446-86a8-42162134f9a9)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/3b3eeb1f-6e58-4707-b15c-b9944f49dba6)



### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/9733bf79-637d-41bc-926b-835580706972)



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/06b2e7cb-0e01-4513-8490-e547e70c9ede)



## RESULT :
Thus the basic DML commands are executed.
