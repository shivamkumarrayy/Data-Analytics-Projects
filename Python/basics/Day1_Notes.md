📒 Day 1 Notes

Date: 23/09/2025
Day: 1

🟠 Morning Session (Python Basics – Variables, Data Types, Input/Output)
🔑 Key Points / Theory

. Variable ek container hota hai jisme data store karte hain.

. Python mein variable declare karne ke liye type specify karna zaroori nahi hai.

. Common data types:

   . int → integers (5, -3)

    . float → decimal numbers (3.14, 0.5)

     . str → text/strings ("Hello")

       .bool → True/False values

. print() → output ke liye

. input() → user se data lene ke liye

. Type casting: int(), float(), str()

💻 Example Code
# variable declaration
name = "Satyam"
age = 22
is_student = True

# printing
print(name, age, is_student)

# user input
user_name = input("Enter your name: ")
user_age = int(input("Enter your age: "))
print("Hello", user_name, "You are", user_age, "years old.")

📤 Output
Satyam 22 True
Hello Ravi You are 21 years old.

⚠️ Mistakes I Made

1.String ko bina quotes likha – error aaya.

2.input() se number liya, par convert nahi kiya to string concatenate ho gaya.

✅ Solution / Learning

1.Strings hamesha quotes me likho.

2.Number input ke liye int(input(...)) ya float(input(...)) use karo.
