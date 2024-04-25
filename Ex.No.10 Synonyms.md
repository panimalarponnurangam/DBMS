# EXP NO 7: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### 1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 

~~~~
CREATE TABLE EMPLOYEE (
    employee_id INT PRIMARY KEY,
    employee_name VARCHAR(255),
    employee_salary DECIMAL(10, 2)
);

INSERT INTO EMPLOYEE (employee_id, employee_name, employee_salary)
VALUES (1, 'Kayal', 50000.00);

INSERT INTO EMPLOYEE (employee_id, employee_name, employee_salary)
VALUES (2, 'Dolly', 60000.00);
~~~~
### OUTPUT:
![318716741-a3baab08-f624-4690-b739-87070a47b9e6](https://github.com/panimalarponnurangam/DBMS/assets/121490826/b1cf387d-c9de-409f-9900-a8898b7aecf6)



### 2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
~~~~
CREATE SYNONYM S1 FOR EMPLOYEE;
~~~~
### OUTPUT:
![318716718-4da68d32-b801-448b-821a-6d33faea53f8](https://github.com/panimalarponnurangam/DBMS/assets/121490826/34f4aef6-840d-4654-8e1b-c8799fbeb3b4)


### 3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
~~~~
SELECT * FROM S1;
~~~~
### OUTPUT:
![318716689-963c4290-5e9f-449b-b356-44b806b8cd8b](https://github.com/panimalarponnurangam/DBMS/assets/121490826/d50190be-2e3c-4ebd-8927-958621dc10c6)


### 4) Drop the synonym.

### SQL QUERY: 
~~~~
DROP SYNONYM S1;
~~~~
### OUTPUT:

![318716660-4a0abc5f-bcd9-4f06-895f-a4e86c47cb91](https://github.com/panimalarponnurangam/DBMS/assets/121490826/fc6ed08c-17b1-48fa-acef-6f5d88e261ae)


### 5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 

~~~~
CREATE TABLE SUPPLIER (
    supplier_id INT PRIMARY KEY,
    supplier_name VARCHAR(255)
);

CREATE SEQUENCE S2;
~~~~~

### OUTPUT:

![318716606-e7b66211-5bf4-4293-8d00-53f01a69d27c](https://github.com/panimalarponnurangam/DBMS/assets/121490826/9c32a591-9922-43d3-8ea3-96e00abd8911)
### 6) insert the data into supplier table use sequence.

### SQL QUERY: 
~~~~
INSERT INTO SUPPLIER (supplier_id, supplier_name)
VALUES (S2.NEXTVAL, 'AB Suppliers');

INSERT INTO SUPPLIER (supplier_id, supplier_name)
VALUES (S2.NEXTVAL, 'CD Suppliers');
~~~~~

### OUTPUT:
![318716563-a592143c-d033-4385-ba95-90edc540ad76](https://github.com/panimalarponnurangam/DBMS/assets/121490826/2beebd0e-3b4d-4c30-904a-76305608fae3)


### 7) Drop the sequence

### SQL QUERY: 
~~~~
DROP SEQUENCE S2;
~~~~
### OUTPUT:

![318716500-d9df85ea-cf61-4cfe-adb3-90a65529a68e](https://github.com/panimalarponnurangam/DBMS/assets/121490826/4a2c87db-f7ab-4833-911a-793fe1bd37de)

## RESULT :
### Thus the sequence and synonym created and used in SQL.
