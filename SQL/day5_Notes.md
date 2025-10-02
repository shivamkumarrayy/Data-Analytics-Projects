# What is a JOIN? – Need for combining multiple tables
Ans: join is used to combine Data, from  two or more  Tables, based on related columns between them.

### 2.  Types of Joins:
  •	INNER JOIN
  •	LEFT JOIN
  •	RIGHT JOIN
  •	FULL OUTER JOIN 
  • SELF JOIN

# 1. INNER JOIN 
> Returns records that have matching values in both tables.

•	Syntax

   SELECT Col_name(s)
   FROM  TableA
   INNER JOIN  TableB
   ON TableA.Col_name = TableB.col_name

•	Example 
      Select * 
      From customer AS c
      INNER JOIN payment AS p
      ON c.customer_id = p.customer_id

# 2. LEFT JOIN 
> Returns all records from the left table, and the matched      
  records from the right table

•	Syntax
   SELECT Col_name(s)
   FROM  TableA
   LEFT JOIN  TableB
   ON TableA.Col_name = TableB.col_name

•	Example 
     Select * 
     From customer AS c
     LEFT  JOIN payment AS p
     ON c.customer_id = p.customer_id


# •	3. RIGHT JOIN
    Returns all records from the right table, and the matched          
    records from the left table

• Syntax
   SELECT Col_name(s)
   FROM  TableA
   RIGHT JOIN  TableB
   ON TableA.Col_name = TableB.col_name

Example 
    Select * 
    From customer AS c
    RIGHT JOIN payment AS ON c.customer_id = p.customer_id

# •4	 FULL JOIN
.  Returns all records when there is a match in either  left  or  right table

•	Syntax
   SELECT Col_name(s)
   FROM  TableA
   LEFT JOIN  TableB
   ON TableA.Col_name = TableB.col_name

•	Example 
Select * 
From customer AS c
LEFT  JOIN payment AS p
ON c.customer_id = p.customer_id

# 5. SELF JOIN
•	 A self-join is a regular join in which a table is joined to itself
•	SELF Joins are powerful for comparing values in a column of rows with the same table
•	Syntax 
    SELECT column_name(s)
    FROM Table AS T1
    JOIN Table AS T2
    ON T1.col_name = T2.col_name



## Difference between WHERE and JOIN condition
In SQL, JOIN is used to link two or more tables together in a single result set, 
and the WHERE clause is used to filter the results based on some criteria
