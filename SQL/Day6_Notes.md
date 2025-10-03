### SUB-QUERIES

A subquery or inner query or nested query allow us to create more complex query from the output the another query
>> Sub query syntax involves two SELECT statements
>>  SYNTAX
     SELECT col_name(s)
     from table_name
     where col_name operator
        (select col_name From table_name where)
>> Q4. Average Salary

 Find names of employees who earn more than average salary.
    SELECT name 
    FROM employees
    WHERE salary > (SELECT AVG(salary) FROM employees);

 # 2.   In FROM clause (as table)

      SELECT dept, MAX(avg_sal) 
      FROM (SELECT dept, AVG(salary) AS avg_sal 
      FROM employees GROUP BY dept) AS temp;


👉 Finds department with highest average salary.


# 3. In SELECT clause (scalar subquery)

SELECT name, (SELECT dept_name FROM departments d 
              WHERE d.dept_id = e.dept_id) AS department
               FROM employees e;

👉 Adds department name next to employee name.

# 4. Operators with Subqueries

# IN →

SELECT name FROM students 
WHERE id IN (SELECT student_id FROM marks WHERE score > 80);


# EXISTS →

SELECT name FROM students s 
WHERE EXISTS (SELECT * FROM marks m WHERE m.student_id = s.id);
