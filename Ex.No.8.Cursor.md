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

PLSQL CURSOR CODE
~~~~
DECLARE
   CURSOR customer_cursor IS
   SELECT customerid,customername,dept,salary
   FROM customer;
   customer_id NUMBER;
   customer_name VARCHAR(50);
   customer_dept VARCHAR(50);
   customer_salary NUMBER;
BEGIN
  OPEN customer_cursor;

  LOOP
    FETCH customer_cursor INTO customer_id, customer_name, customer_dept, customer_salary;

    EXIT WHEN customer_cursor%NOTFOUND;

    DBMS_OUTPUT.PUT_LINE('Customer ID: ' || customer_id);
    DBMS_OUTPUT.PUT_LINE('Customer Name: ' || customer_name);
    DBMS_OUTPUT.PUT_LINE('Department: ' || customer_dept);
    DBMS_OUTPUT.PUT_LINE('Salary: ' || customer_salary);
  END LOOP;

  CLOSE customer_cursor;
END;
~~~~
OUTPUT
![image](https://github.com/panimalarponnurangam/DBMS/assets/121490826/b868cb07-f1fc-43e5-a78b-8b2a74f9ad9e)

### Result:
Thust the program was performed sucessfully.
