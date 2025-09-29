🗄 SQL – GROUP BY & HAVING
🔹 GROUP BY

Aggregate functions ko groups ke basis par apply karta hai.

Example:

SELECT department, SUM(salary) 
FROM employees 
GROUP BY department;


👉 Output: Har department ki total salary show karega.

🔹 HAVING

WHERE → rows filter karta hai

HAVING → groups filter karta hai

Example:

SELECT department, COUNT(*) 
FROM employees 
GROUP BY department 
HAVING COUNT(*) > 5;


👉 Output: Sirf wahi departments jisme 5 se zyada employees hain.

✅ Solved Question 3

Q: Find average marks of each subject but only include subjects where average > 50.

SELECT subject, AVG(marks) 
FROM students 
GROUP BY subject 
HAVING AVG(marks) > 50;

✅ Solved Question 4

Q: Count how many employees are in each department.

SELECT department, COUNT(*) 
FROM employees 
GROUP BY department;

🔑 Key Points to Remember

Strings: Slicing → start included, end excluded

Functions: Default parameters use hote hain jab value na di ho

GROUP BY: Rows ko groups me todta hai

HAVING: Groups ko filter karta hai (jaise COUNT, AVG ke basis par)

📒 Tum apne notes ke end me ek Mistakes Section banao:

Q1 (string slicing) galat hua tha → revise slicing

Q5 (HAVING clause) galat hua tha → revise WHERE vs HAVING



.
👇

🔹 Q9. Write an SQL query to find the maximum salary in each department.
SELECT department, MAX(salary) AS max_salary
FROM employees
GROUP BY department;


✅ Explanation:

GROUP BY department → department-wise grouping.

MAX(salary) → har department ka highest salary nikalta hai.

🔹 Q10. Write an SQL query to count the number of students in each class.
SELECT class, COUNT(*) AS total_students
FROM students
GROUP BY class;


✅ Explanation:

COUNT(*) → rows count karega.

GROUP BY class → har class ke students ki ginti.

🔹 Q11. Write an SQL query to display only those departments where the average salary is greater than 50,000.
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;


✅ Explanation:

AVG(salary) → average salary nikalta hai.

HAVING → group ke result pe condition lagane ke liye use hota hai (WHERE ki tarah, but groups ke liye).

🔹 Q12. Write an SQL query to find the total marks obtained by students in each subject, but only show subjects where total marks > 200.
SELECT subject, SUM(marks) AS total_marks
FROM results
GROUP BY subject
HAVING SUM(marks) > 200;


✅ Explanation:

SUM(marks) → har subject ka total nikalta hai.

HAVING SUM(marks) > 200 → sirf wahi subjects dikhata hai jaha total 200 se jyada ho.
