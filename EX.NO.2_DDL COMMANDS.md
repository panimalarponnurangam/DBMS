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

~~~
create table students(
    registernumber integer,
    name varchar(50),
    age integer,
    address varchar(60),
    phonenumber integer
    
);
~~~

### OUTPUT:

![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/05d36dc2-1e33-4dcb-be4b-38880aa4330c)

### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
~~~
alter table students
add department char(80);
~~~


### OUTPUT:
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/72a756c9-0369-4ed9-ad8e-d69a5f7b40fd)


### 3) Rename the student table to mystudent

### SQL QUERY: 
~~~
alter table students rename to mystudent;
~~~
### OUTPUT:
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/085fc297-e9c7-4a72-96d9-4b86c0bdc25e)

### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
~~~
truncate table mystudent;
~~~

### OUTPUT:
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/8dd25f18-38a2-4180-9c23-be659cf7499f)

### 5) Drop the mystudent table
 
### SQL QUERY: 
~~~
drop table mystudent;
~~~
### OUTPUT:
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/be1350e9-a09a-4aa9-a947-7b5ac8f8a69a)








## Result:
         Thus the basic DDL commands in SQL are executed. 


