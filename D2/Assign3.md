Database Technologies – Assignment 3
Note : To solve below queries use “hr” database


1. Write a query to get unique department ID from employee table.

sol. SELECT DISTINCT DEPARTMENT_ID
     FROM employees;

2. Write a query to get all the employee’s details from the
employees table displaying the first names in descending
order.

sol. SELECT *
     FROM employees
     ORDER BY FIRST_NAME DESC;

3. Write a query to get the employee ID, names
(first_name and last_name), salary in ascending order of
salary.

sol. SELECT employee_id ,first_name,last_name,salary
     FROM employees
     ORDER BY salary ASC;

4. Display first name and joining date of the employees
who are either IT Programmer or Sales Man.

sol. SELECT first_name , hire_date
     FROM employees
     WHERE job_id='it_prog' or job_id='fi_account';

5. Display details of employees with employee ID 150 or 160.

sol. SELECT *
     FROM employees
     WHERE employee_id=150 or employee_id=160;

6. Display first name, salary, commission pct, and hire date
for employees with salary less than 10000.

sol. SELECT first_name, salary, commission_pct, hire_date
     FROM employees
     WHERE salary<10000;

7. Display employees where the first name or last name
starts with S.

sol. SELECT *
     FROM employees
     WHERE first_name LIKE 's%' OR last_name Like's%';

8. Display details of jobs in the descending order of the title.

sol. SELECT *
     FROM jobs
     ORDER BY job_title DESC;

9. Display the details of the employees from department 30,
earning the salary greater 10000 but do not receive the
commission.

sol. SELECT *
     FROM employees
     WHERE department_id=30 AND salary>10000 AND (commission_pct IS NULL OR commission_pct<=0.0);

10.Display the details of employees reporting to the managers
with employee id 100 and 120.

sol. SELECT *
     FROM employees
     WHERE manager_id=100 or manager_id=120;

11. Display the unique country_id from locations table.

sol. SELECT DISTINCT country_id
     FROM locations;

12. Display all employees whose have the job_id as IT_PROG and FI_ACCOUNT.

sol. SELECT * 
     FROM employees
     WHERE job_id='IT_PROG' OR job_id='FI_ACCOUNT';

13. Display all countries in ascending order.

sol. SELECT *
     FROM countries
     ORDER BY country_name ASC;