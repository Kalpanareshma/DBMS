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
### 1) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
create table students(
    registernumber integer,
    name varchar(50),
    age integer,
    address varchar(60),
    phonenumber integer
    
);
```


### OUTPUT:
![dbms1](https://github.com/DrUmaRaniV/DBMS/assets/122040453/281bf6a0-86e1-485d-8a0a-c76b9fdf5c40)

### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table students
add department char(80);
```

### OUTPUT:
![dbms1](https://github.com/DrUmaRaniV/DBMS/assets/122040453/96cffa5d-f454-4b72-8868-3bf6a651c1c6)

### 3) Rename the student table to mystudent

### SQL QUERY: 
```
alter table students rename to mystudent;
```
### OUTPUT:
![dbms2](https://github.com/DrUmaRaniV/DBMS/assets/122040453/48bcb862-c006-431f-b831-9b743a898511)

### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table students
```
### OUTPUT:
![dbms3](https://github.com/DrUmaRaniV/DBMS/assets/122040453/6fc6f9bc-6069-469b-a744-1a2f7e80fa48)


### 5) Drop the mystudent table
 
### SQL QUERY: 
```
drop table students;
```
### OUTPUT:
![dbms3](https://github.com/DrUmaRaniV/DBMS/assets/122040453/6fb96d7f-ebff-4600-89ff-b4678dd9a4a9)











## Result:
         Thus the basic DDL commands in SQL are executed. 


