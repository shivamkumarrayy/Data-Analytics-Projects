📘 Day 4 Notes – Python Strings & Functions + SQL GROUP BY & HAVING
🐍 Python Strings
🔹 Definition

String ek sequence of characters hota hai jo " " ya ' ' ke andar likha jata hai.

🔹 Indexing & Slicing

Indexing → Position access karna (s[0], s[-1])

Slicing → Substring nikalna (s[start:end], end exclude hota hai)

Example:

s = "Python"
print(s[0])     # P
print(s[-1])    # n
print(s[1:4])   # yth


👉 Output:

P
n
yth

🔹 Common String Functions
s = "hello world"
print(len(s))          # 11
print(s.upper())       # HELLO WORLD
print(s.lower())       # hello world
print(s.replace("world","Python"))  # hello Python
print("hello" in s)    # True

✅ Solved Question 1

Q: Write a Python program to reverse a string.

s = "Python"
print(s[::-1])


👉 Output: nohtyP

🐍 Python Functions
🔹 Definition

Function ek block of code hota hai jo reuse kiya ja sakta hai.

🔹 Defining & Calling Function
def greet():
    print("Hello")
    
greet()


👉 Output: Hello

🔹 Function with Parameters
def add(a, b):
    return a + b

print(add(3, 4))   # 7

🔹 Default Parameters
def add(a, b=2):
    return a + b

print(add(3))   # 5
print(add(3, 4)) # 7

✅ Solved Question 2

Q: Write a function to check whether a number is even or odd.

def even_odd(num):
    if num % 2 == 0:
        return "Even"
    else:
        return "Odd"

print(even_odd(7))   # Odd
print(even_odd(10))  # Even
