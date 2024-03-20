# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb

### SQL QUERY:
```
create database studentdbb;
```

### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/ec949e17-0b6a-4a88-98a9-ddd979beebb3)


### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY:
```
create table student(RegisterNumber int,Name varchar(100),Age int,Address varchar(250),PhoneNumber int) ;
```


### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/caf5bc60-b1cc-4fd7-b6d8-401278faa3f2)


### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
 alter table student add dept varchar(20);
```
### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/12faa665-3e6d-4e0b-b605-6745f17f5693)


### 4) Rename the student table to mystudent

### SQL QUERY: 
```
rename table student to mystudent;
```
### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/c41a6b08-9cd4-41e9-a59c-29bb45f11e70)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table mystudent;
```
### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/58f7cf60-c629-4afa-945f-64db7260eacc)

### 6) Drop the mystudent table
 
### SQL QUERY: 
```
drop table mystudent;
```
### OUTPUT:
![image](https://github.com/Kalpanareshma/DBMS/assets/122040453/712205d0-5a95-4f72-8857-629732f2b6ab)
## Result:
         Thus the basic DDL commands in SQL are executed. 


