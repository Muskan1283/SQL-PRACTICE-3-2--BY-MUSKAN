# SQL-PRACTICE-3-2--BY-MUSKAN

CREATE DATABASE PROJECT3
USE PROJECT3

CREATE TABLE EMP_DETAILS(E_ID INT PRIMARY KEY IDENTITY not null, E_NAME VARCHAR(20) ,
E_SALARY MONEY ,E_DEPT VARCHAR(20),E_GENDER VARCHAR(20) )



INSERT INTO EMP_DETAIL VALUES
('Vandana',25000,'IT','Female'),
('Mohan',30000,'HR','Male'),
('Jyoti',35000,'IT','Female'),
('Vimla',40000,'CS','Female'),
('Gita',20000,'IT','Female'),
('Jacky',45000,'HR','Male')

CREATE TABLE DEPT_DETAIL (DEPT_ID int primary key identity not null,DEPT_Name varchar(20),DEPT_No int )

insert into  DEPT_DETAIL  values
('IT',2),
('HR',1),
('CS',4),
('IT',3),
('HR',6),
('IT',5)

SELECT * INTO DEPT_DETAILS FROM EMP_DETAIL

SELECT *FROM EMP_DETAIL
UNION
select * from DEPT_DETAILS

select E_Name ,E_salary from EMP_DETAIL group  by E_NAME ,E_SALARY order by E_salary desc

select * into EMP_DETAILS from DEPT_DETAIL WHERE 1=0

select * from EMP_DETAIL where E_SALARY between 35000 and 45000

select * from EMP_DETAILS
union 
select * from DEPT_DETAIL 

select * from EMP_DETAILS
INTERSECT
select * from DEPT_DETAIL

SELECT*FROM DEPT_DETAILS WHERE E_NAME NOT IN (SELECT E_NAME FROM EMP_DETAILS)

 
select E_NAME, sum(E_SALARY) as totalsal from EMP_DETAIL group by E_NAME having sum(E_ID)>=2

select count(E_salary) totalemp from EMP_DETAIL

select min(E_SALARY) totalsal from EMP_DETAIL

select max(E_SALARY) totalsal from EMP_DETAIL

select sum(E_SALARY) totalsal from EMP_DETAIL

select avg(E_SALARY) totalsal from EMP_DETAIL
