# MySQL-Assignment-1


-- Q1-Write an SQL command that will create a table named Friend with the following fields and types: - idno NUMERIC (10), fname VARCHAR (24), address VARCHAR (30), age NUMERIC (10), giftvalue NUMERIC (10, 2)

create table friends (
idno NUMERIC (10),
fname VARCHAR (24),
Address VARCHAR (30),
age NUMERIC (10),
giftvalue NUMERIC (10, 2));

select*from friends;

-- Q2-Insert the following items in the table you have created
-- Idno	FName	Address	Age	Giftvalue
-- 01	Ram	Dwarka sector 10	41	200
-- 02	Sita	Janakpuri block c	26	250
-- 03	Rajesh	Dwarka sector 15	23	200
-- 04	Ajit	Noida sector 11	35	150
-- 05	Rita	Noida sector 11	40	200


INSERT INTO friends VALUES('01','RAM','Dwarka sector 10','41','200');
INSERT INTO friends VALUES('02','Sita','Janakpuri block C','26','250');
INSERT INTO friends VALUES('03','Rajesh','Dwarka sector 15','23','200');
INSERT INTO friends VALUES('04','Ajit','Noida sector 11','35','150');
INSERT INTO friends VALUES('05','Rita','Noida sector 11','40','200');

-- Q3-Write an SQL query to display all the records;
select*from friends;

-- Q4-Write an SQL query to display all the records where age is >40.
select*from friends where age>40;

-- Q5-Write an SQL query to display Fname, Age from the table.
select fname,Age from friends;

-- Q6-Write an SQL query to display Write an SQL query to display Fname, Age, Gift value where Age > 35 from the table. the table.
select Fname,Age,Giftvalue from friends where Age>'35';

-- Q7-Write an SQL query to display all record where Gift vale is > 200 and Age >20.
select* from friends where giftvalue>200 and age>20;

-- Q8-Write an SQL query to display all record where Gift vale is > 200 or Age >20.
select* from friends where giftvalue>200 or age>20;


-- AASIGNMENT 2
-- Q1-Create a table with the following specifications
-- Field name	Data type
-- EMPID	Numeric(10)
-- DEPT	CHAR(5)
-- EMPNAME	VARCHAR(15)
-- ADDRESS	VARCHAR(30)
-- SALARY	NUMERIC(7)

CREATE table employeeinfo(
EMPID NUMERIC(10),
DEPT CHAR(5),
EPNAME VARCHAR(15),
ADDRESS VARCHAR(30),
SALARY NUMERIC(7));
select * from employeeinfo;

-- Q2-Make the following entries in the table
-- EMPID	DEPT	EMPNAME	ADDRESS	SALARY
-- 101	RD01	Prince	Park Way	15000
-- 102	RD01	Harry	Pebble Street	12000
-- 103	RD02	Tom 	Park Avenue	11000
-- 104	RD02	Susan	Model Town	10000
-- 105	ED01	Mark	Victor Crescent	10000
-- 107	GR01	Robert	Downtown Cross	14000
-- 108	RD03	Philip	Park Avenue	15000
-- 109	RD03	Henry	Malibu Beach	14000
-- 110	AD01	Frank	St. Peters Lane	7000

INSERT INTO employeeinfo values (101,'RD01','Prince','Park Way',15000);
INSERT INTO employeeinfo values (102,'RD01','Harry','Pebble Street',12000);
INSERT INTO employeeinfo values (103,'RD02','Tom','Park Avenue',11000);
INSERT INTO employeeinfo values (104,'RD02','Susan','Model Town',10000);
INSERT INTO employeeinfo values (105,'ED01','Mark','Victor Crescent',10000);
INSERT INTO employeeinfo values (106,'AD01','Francis','Chelmsford Park',13000);
INSERT INTO employeeinfo values (107,'GR01','Robert','Downtown Cross',14000);
INSERT INTO employeeinfo values (108,'RD03','Philip','Park Avenue',15000);
INSERT INTO employeeinfo values (109,'RD03','Henry','Malibu Beach',14000);
INSERT INTO employeeinfo values (110,'AD01','Frank','St. Peters Lane',7000);
select*from employeeinfo;

-- Q2-2.	Write an SQL query to display all the records where RD01is the department.
select*from employeeinfo where dept='RD01';

-- Q3-3.	Write an SQL query to display EMPNAME, DEPT, Salary from the table.
select EPNAME,DEPT,Salary from employeeinfo;

-- Q4-4.	Write an SQL query to display EMPNAME, DEPT, Salary from the table where salary is greater than 13000.
select EPNAME,DEPT,Salary from employeeinfo where salary>13000;

-- Q5-5.	Write an SQL query to display the record of those employees who lives in Park Avenue.
select * from employeeinfo where address='Park Avenue';

-- Q6-6.	Display name, id of those employees who salary is 15000 and lives in Park Avenue
select EPNAME,EMPID from employeeinfo where salary=15000 and address='Park Avenue';

-- Q7-7.	Find names for all employees who work for the department RD01.
select EPNAME from employeeinfo where DEPT='RD01';

-- Q8-How many employees work in department starting from RD.
select*from employeeinfo where DEPT like 'RD%';

-- Q9-What is the maximum and minimum of the salaries.
select max(salary) from employeeinfo;
select min(salary) from employeeinfo;


-- Q10-Name the employees and their department whose salaries are greater than 12000.
select EPNAME,DEPT from employeeinfo where salary>12000;

-- Q11-List the employees in increasing order of their salaries.
select*from employeeinfo order by salary;

-- Q12-Modify the table so that Susan is assigned department AD01.
update employeeinfo set DEPT='AD01' where EPNAME='Susan';

-- Q13-Name the employee in department RD03 who lives in Park Avenue
select EPNAME from employeeinfo where DEPT='RD03' and address='Park Avenue';

-- Q14-Find the Average salary.
select avg(salary) from employeeinfo;

-- Q15-Count the number of employees. 
select count(salary) from employeeinfo;

-- Q16-Find details of those employees whose salary is > the average salary for all employees
select*from employeeinfo where salary>12100;

-- ASSIGNMENT 3

-- Q1-1.	Write an SQL command that will create a table named FriendNew with the following fields and types:  idno NUMERIC(10)  PRIMARY KEY, fname VARCHAR(24), address VARCHAR(30),  age NUMERIC(10) , giftvalue NUMERIC(10,2).
create table friendsnew (
idno numeric(10),
fname varchar(24) primary key,
Address varchar(30),
Age numeric(10),
Giftvalue numeric(10,2))

select *from friendsnew;

-- Q2-Insert the following items in the table you have created
-- Idno	FName	Address	Age	Giftvalue
-- 01	Ram	Dwarka sector 10	41	200
-- 02	Sita	Janakpuri block c	26	250.80
-- 03	Rajesh	Dwarka sector 15	23	200
-- 04	Ajit	Noida sector 11	35	150.50
-- 05	Rita	Noida sector 11	40	200


INSERT INTO friendsnew VALUES('01','RAM','Dwarka sector 10','41','200');
INSERT INTO friendsnew VALUES('02','Sita','Janakpuri block C','26','250.80');
INSERT INTO friendsnew VALUES('03','Rajesh','Dwarka sector 15','23','200');
INSERT INTO friendsnew VALUES('04','Ajit','Noida sector 11','35','150.50');
INSERT INTO friendsnew VALUES('05','Rita','Noida sector 11','40','200');

select*from friendsnew;

-- Q3-3.	Write a SQL query to display all the records whose name starts with R.
select*from friendsnew where fname like'R%';

-- Q4-Write an SQL query that will insert a complete record into the Friend table with these values for the respective fields:  '123', 'Anil', 'Dwarka Sector 11', 23, 29.99.
INSERT INTO friendsnew values ('123', 'Anil', 'Dwarka Sector 11', 23, 29.99);

-- Q5-Write an SQL query to change the age of Sita to 28.
update friendsnew set age=28 where fname='sita';

-- Q6-Write an SQL query to delete the record with  idno 123.
delete from friendsnew where idno=123;

-- Q7-Write an SQL query that will update the giftvalue to 49.99 for all people in the Friend table whose age is equal to or greater than 31 years.
update friendsnew set giftvalue=49.99 where age>=31;

-- Q8-Write an SQL query that will add a field named City to the Friend table with datatype as varchar and size equal to 15.
ALTER table friendsnew Add city varchar(15);

-- Q9-	Add the name of the city for all the records in the table.
update friendsnew set city='Delhi';

-- Q10-Write a SQL query to display fname and age of all the records in ascending order.
select fname,age from friendsnew order by fname;

-- Q11-Write SQL query to get the cumulative giftvalue for all records.
select sum(giftvalue) from friendsnew;

-- Q12-Write a query to average of the age of all the friends under the heading ‘Average Age’.
select avg(Age) 'Average Age' from friendsnew;

-- Q13-Write a query to display the name and age of the youngest member.
select fname,Age from friendsnew where age=(select min(Age) from friendsnew);

-- Q14-Write a query to count the number of candidates whose age in more than 30 years.
select count(*)from friendsnew where age>30;

-- Q15-Write a query to display the name and giftvalue of the record with highest gift value.
select fname,giftvalue from friendsnew where giftvalue=(select max(giftvalue)from friendsnew);

-- Q16-Write an SQL query that will delete all records from the Friend table whose idno is 123.
delete from friendsnew where idno=123;

-- Q17-Write a query to delete all the records. 
drop table friendsnew;
