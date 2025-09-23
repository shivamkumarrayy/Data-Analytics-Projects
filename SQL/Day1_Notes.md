🟠 Night Session (SQL Basics – SELECT & WHERE)
🔑 Key Points / Theory

. SELECT → Columns choose karne ke liye

. WHERE → Filter karne ke liye conditions lagate hain

. Operators: =, >, <, >=, <=, <> (not equal)

💻 Example Queries
-- table: students(id, name, age, marks)

-- sab students ke naam
SELECT name FROM students;

-- marks > 50 wale students
SELECT name, marks FROM students WHERE marks > 50;

-- ek student ka record (id = 3)
SELECT * FROM students WHERE id = 3;

📤 Output
Ravi
Aman 65
id=3 | Priya | 20 | 72

⚠️ Mistakes I Made

1.Query me semicolon lagana bhool gaya.

2.Column name galat likha – error aaya.

✅ Solution / Learning

1.Har SQL statement end me ; lagao.

2.Column names check karke likho.

🟢 Next Steps (Day 2)

. Python: Operators (arithmetic, relational, logical)

. SQL: ORDER BY, LIMIT
