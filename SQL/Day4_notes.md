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
