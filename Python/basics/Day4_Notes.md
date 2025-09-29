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

# Write a Python program to check whether a string is a palindrome or not.
👉 Example: "madam" → Palindrome

## solution
x = input("Enter the string: ")

# reverse string
y = x[::-1]

if y == x:
    print("String is palindrome")
else:
    print("String is not palindrome")


🔹 Q2. Take a string as input and count how many vowels (a, e, i, o, u) are in it.
def count_vowels(s):
    vowels = "aeiouAEIOU"
    count = 0
    for ch in s:
        if ch in vowels:
            count += 1
    return count

# Example
text = "Hello World"
print("Number of vowels:", count_vowels(text))  

🔹 Q3. Write a Python program to remove all spaces from a given string.
def remove_spaces(s):
    return s.replace(" ", "")

# Example
text = "Python is fun"
print(remove_spaces(text))

.

🔹 Q4. Write a Python program that converts the first character of every word in a string to uppercase.
def capitalize_words(s):
    return s.title()

# Example
text = "hello world from python"
print(capitalize_words(text))


✅ Output:

Hello World From Python




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





#  Q6. Write a function is_prime(num) that returns True if the number is prime, otherwise False.
# solution
def is_prime(num):
    count = 0
    for i in range(1,num + 1):
        if  num%i==0:
             count= count + 1
    if count == 2:
        return True
    else:
        return False
num = int(input("enter a number: "))
z=is_prime(num)
if z==1:
    print("True")
else:
    print("False")
