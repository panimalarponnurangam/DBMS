# Ex. No: 6 PL/SQL program using Cursor 
### DATE: 
### AIM: To create PL/SQL program to display the customer table 

### Steps:
1. Declare the variable  in Declare section.
2. Fetch the variable with datatype similar to data type in cursor 
3. Create a cursor to select all rows from customers table.
4. Display the result 
5. End the begin section.

### Program:
Create employee table:
~~~
CREATE TABLE customer (
  customerid NUMBER,
  customername VARCHAR(10),
  dept VARCHAR(10),
  salary NUMBER
);

INSERT INTO customer VALUES (1, 'Dhanu', 'HR', 100000);
INSERT INTO customer VALUES (2, 'Amutha', 'Staff', 80000);
select * from customer;
~~~

### Output:
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/2b1f0eef-3699-4356-af64-1f4bccc5b125)


### Result:
Thust the program was performed sucessfully.
