# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/2671ac5d-aaa0-47ad-a40e-b98aec9fd58e)

### Q2) Insert three rows into emploee table 


### QUERY:
```
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/df4f6c33-3865-42f5-8eea-7983a4503526)


### Q3) Start the transaction and create a save point s1.

### QUERY:
```
savepoint A;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/0e6183d9-cffa-4a4d-981b-8ca8cce76155)


### Q4) Perform insertion into employee table.

### QUERY:
```
insert into employee(4,'Robin','EniesLobby');
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/02ed557b-5ff4-4136-af8f-2dfe95bb92c4)



### Q5)	Display the employee table and create a save point s2 .


### QUERY:
```
sql
select * from employee;
savepoint s2;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ad07dad2-f802-4b6f-bf2d-0b6e5f271b2d)



### Q6)	Perform updation on any one of the row.


### QUERY:
```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/31725e7d-70e7-4594-b473-a86ef8bc54f0)


### Q7) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```



### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/9dd9f3a6-49dd-4fbd-8f80-5aa0be6eb063)



### Q8) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/40bbafaf-64f0-485f-a6ac-cdc0216185ed)



### Q9) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/41617233-9078-4f54-9e9b-a128a48cc4e1)



### Q10)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/4c1ff36f-d7d7-4520-96dd-8d1286acf99b)
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/de5d6fae-af70-4d99-a5fa-97c3110e75da)




### Q11) Check the user access and display the result 


### QUERY:
```
SHOW GRANTS FOR new_user;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/9e740f36-2b2f-46a7-aecf-42a365a04f88)


### Q12) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/b096ddeb-f791-4ae9-9c80-52f253c5c68f)



## RESULT :
Thus the basic TCL and DCL commands are executed.
