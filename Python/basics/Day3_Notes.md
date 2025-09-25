📘 Day 3 Notes – Python Loops & SQL Aggregate Functions
🐍 Python Loops
1. For Loop

Jab iterations ka count pehle se pata ho, tab use hota hai.

Syntax:

for i in range(start, end, step):
    # code
Example:
for i in range(1, 5):
    print(i)    # Output: 1 2 3 4

2. While Loop
   Jab iterations ka count unknown ho, tab use hota hai.
Syntax:
      while condition:
 # code
Example:
x = 0
while x < 3:
    print("Hi")
    x += 1
# Output: Hi Hi Hi

3. Loop Control Statements

break → loop ko turant rok deta hai

continue → current iteration skip karke next pe jata hai

pass → kuch nahi karta (placeholder)

#### PRACTICE QUESTIONS

Q1. for i in range(1, 5): print(i, end=" ")
✅ Answer: c. 1 2 3 4
👉 Explanation: range(1,5) numbers 1 se 4 tak generate karta hai (5 exclude hota hai).

Q2. Best loop when iterations unknown?
✅ Answer: b. while loop
👉 Explanation: while loop tab use hota hai jab stopping condition pehle se fixed nahi hoti.

Q3.
x = 0
while x < 3:
    print("Hi")
    x += 1
✅ Answer: a. Hi Hi Hi
👉 Explanation: Loop tab tak chalega jab tak x < 3 hai → 3 times run karega.
