SQL (ORDER BY, LIMIT, LIKE)
🔑 Key Points

ORDER BY → sorting ke liye

ASC (ascending, default), DESC (descending)

LIMIT → top n rows dikhata hai

LIKE → pattern matching

% → multiple characters

_ → single character

💻 Example Queries
-- Students table
id | name   | marks
---+--------+------
1  | Amit   | 85
2  | Priya  | 92
3  | Pooja  | 76
4  | Rahul  | 89
5  | Preeti | 95

-- ORDER BY
SELECT * FROM students ORDER BY marks DESC;

-- LIMIT
SELECT * FROM students ORDER BY marks DESC LIMIT 3; 

-- LIKE
SELECT * FROM students WHERE name LIKE 'P%';   -- starts with P
SELECT * FROM students WHERE name LIKE '%a';   -- ends with a
SELECT * FROM students WHERE name LIKE '%oo%'; -- contains "oo"

⚠️ Mistakes I Made

ASC aur DESC me confuse ho gaya (top students ke liye hamesha DESC).

✅ Solutions / Learnings

Jab bhi query likho, pehle condition read karo (>=, <=, DESC).

'OFFSET' ko use kiya jata 'LIMIT' ke sath taki kitna row ke bad data show ho

PRACTICE QUESTIONS

Q4.
SELECT * FROM students WHERE marks >= 80 AND marks <= 90;
✅ Correct Answer: (a) 80 aur 90 ke beech ke students ko dikhayegi

Q5:
SELECT * FROM students ORDER BY marks DESC LIMIT 1;

✅ Correct Answer: (b) Highest marks wale student ko dikhayegi

Q6:
SELECT * FROM students WHERE name LIKE '%a';

✅ Correct Answer: (b) Sirf un students ke naam jo a pe end hote hain
