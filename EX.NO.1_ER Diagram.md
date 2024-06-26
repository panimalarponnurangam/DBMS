# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![Screenshot 2024-03-13 112300](https://github.com/panimalarponnurangam/DBMS/assets/121490826/eb019739-d411-44af-87c2-c6adcd5a6bff)


### Relational model

![Screenshot 2024-03-13 113454](https://github.com/panimalarponnurangam/DBMS/assets/121490826/276c1dbc-b541-42f0-87cd-f36978a54807)

### SQL DDL Schema 
````
CREATE TABLE student
(
  DOB INT NOT NULL,
  name INT NOT NULL,
  student_id INT NOT NULL,
  PRIMARY KEY (student_id)
);

CREATE TABLE facutly
(
  f_id INT NOT NULL,
  name INT NOT NULL,
  department INT NOT NULL,
  salary INT NOT NULL,
  PRIMARY KEY (f_id)
);

CREATE TABLE subject
(
  subject_id INT NOT NULL,
  subject_name INT NOT NULL,
  PRIMARY KEY (subject_id)
);

CREATE TABLE course
(
  course_id INT NOT NULL,
  duration INT NOT NULL,
  course_name INT NOT NULL,
  PRIMARY KEY (course_id)
);

CREATE TABLE department
(
  department_id INT NOT NULL,
  d_name INT NOT NULL,
  PRIMARY KEY (department_id)
);

CREATE TABLE exams
(
  date INT NOT NULL,
  time INT NOT NULL,
  exam_code INT NOT NULL,
  PRIMARY KEY (exam_code)
);

CREATE TABLE student_phone_no
(
  phone_no INT NOT NULL,
  student_id INT NOT NULL,
  PRIMARY KEY (phone_no, student_id),
  FOREIGN KEY (student_id) REFERENCES student(student_id)
);

CREATE TABLE facutly_mobile_no
(
  mobile_no INT NOT NULL,
  f_id INT NOT NULL,
  PRIMARY KEY (mobile_no, f_id),
  FOREIGN KEY (f_id) REFERENCES facutly(f_id)
);
````

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
