# EX 3 SubQueries, Views and Joins 


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

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/635bedc8-6487-40c4-8aad-4b4df7f92509)



### OUTPUT:


![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/55d13c6b-0bbf-4443-a5d7-a3266f597e4f)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/92129740-86a8-4504-831f-c3eb49722c7f)



### OUTPUT:


![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/33751014-9f8a-4cff-91d3-777bc3863536)


### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/220cb8b2-ed09-4f5d-9f80-178617fceadb)


### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/c4e13ecb-1142-4e66-924c-46f38c457ad0)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/9703b891-1c50-4c5c-9db9-281c846d417b)


### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/33e47964-2a1f-489c-bd74-55f4b5788e08)


### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:


### OUTPUT:

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/2ce5d45b-b377-4aef-9bfc-ad22fb1ac5e0)



### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/8fce490c-fe82-4ec7-98f0-dfea9b43b16c)


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

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/3e81bb4e-d880-49ce-b355-901347f07ed7)



### OUTPUT:



![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/cec1b48d-29ba-4ede-9b1b-5a2368473732)


### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/caf7a537-7f70-4988-a9ce-ea272c077336)


### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/4c75dcce-586a-45a9-b924-808946ef2328)


### Q9) Perform Natural join on both tables

### QUERY:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/7e0e8f4e-922c-46e0-ab0e-3cd2476404a5)



### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/85b8517a-820c-4d67-bbf3-b172bdfb33ba)


### Q10) Perform Left and right join on both tables

### QUERY:
Left Join:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/e51cee44-86b0-4dea-b94c-2e8b85739e56)



### OUTPUT:

![image](https://github.com/Thenmozhi-Palanisamy/EX-3-SubQueries-Views-and-Joins/assets/95198708/fccf9c12-1e7a-404e-ba54-103aad0c16ee)


## RESULT:

Thus the  SubQueries, Views and Joins are done successfully.
