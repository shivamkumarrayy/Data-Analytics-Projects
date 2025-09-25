 🗄 SQL Aggregate Functions

Aggregate functions → Multiple rows ko process karke ek single value return karte hain.

3. COUNT(column_name) → NULL ko chhodkar total rows count karega

SELECT COUNT(name) FROM students;


2. SUM(column_name) → values ka sum nikalta hai

SELECT SUM(marks) FROM students;


3. AVG(column_name) → average value return karta hai

SELECT AVG(salary) FROM employees;


4. MIN(column_name) → lowest value return karta hai

SELECT MIN(price) FROM products;


5. MAX(column_name) → highest value return karta hai

SELECT MAX(age) FROM users;

🔑 Important Points

# COUNT(*) → NULL values ke sath bhi rows count karta hai

# COUNT(column) → NULL values ko ignore karta hai

# Loops me for → known iterations aur while → unknown iterations


# PRACTICE QUESTIONS

Q4. MAX(salary) return karega?
✅ Answer: a. Highest value
👉 Explanation: MAX() column me sabse badi value nikalta hai.

Q5. Average salary nikalne ka sahi tarika?
✅ Answer: c. Both a and b
👉 Explanation: AVG(salary) direct average nikalta hai, aur (SUM/COUNT) se bhi wahi result milega.

Q6. COUNT(name) kya karega agar NULL values hain?
✅ Answer: b. Excludes NULL values
👉 Explanation: COUNT(column) sirf non-NULL entries count karta hai.
