# Set
-- Sets are used to store multiple items in a single variable.
-- A set is a collection which is unordered, unchangeable, and unindexed.
-- Sets cannot have two items with the same value.(canont contain duplicate values).
-- set = {"apple", "banana", "cherry"}

#   Access Items in set 
 --- for x in thisset:
 #  Add Items
 -- To add one item to a set use the  'add()' method.
 --  thisset.add("orange")
 # To add items from another set into the current set, use the 'update()' method.and can 
 # also add  it can be any iterable object (tuples, lists, dictionaries etc.).
 --thisset = {"apple", "banana", "cherry"}
   tropical = {"pineapple", "mango", "papaya"}
   
   thisset.update(tropical)
#  Remove Item
To remove an item in a set, use the remove(), or the discard() method.
agar element set me nahi hai to error dega ,remove() : - set.remove(2)
or discard() me error nahi dega: - set.discard(1)

# Remove a random item by using the pop() method:
  lekin koi bhi element delete ho sakta hai
  thisset = {"apple", "banana", "cherry"}
  x = thisset.pop()


  # The clear() method empties the set: 
     set ko empty karta hai lekin delete nahi karta hai
  # lekin del keyword me set delete ho jata hai
     e.g.  del set

# Join Sets
There are several ways to join two or more sets in Python.

# The union() and update() methods joins all items from both sets./ for union only set3 = set1.union(set2) or set3 = set1 | set2

# The intersection() method keeps ONLY the duplicates.// set3 = set1.intersection(set2) or set3 = set1 & set2

# The difference() method keeps the items from the first set that are not in the other set(s).// set3 = set1.difference(set2) or set3 = set1 - set2

# The symmetric_difference() method keeps all items EXCEPT the duplicates.// set3 = set1.symmetric_difference(set2) or set3 = set1 ^ set2


# 1. Creating a Set
s = {1, 2, 3}
empty = set()   # Correct way (not {})


👉 {} se empty set nahi banta, wo dict hota hai.

# 2. Adding Elements
s = {1, 2}
s.add(3)               # {1, 2, 3}
s.update([4, 5])       # {1, 2, 3, 4, 5}


👉 add() ek element, update() multiple elements ke liye.

# 3. Removing Elements
s = {1, 2, 3}
s.remove(2)     # {1, 3} (Error if not found)
s.discard(10)   # No error
s.pop()         # Removes random element
s.clear()       # Empty set


👉 Safe removal ke liye discard() use karo.

# 4. Set Operations
s1 = {1, 2, 3}
s2 = {3, 4, 5}

print(s1.union(s2))        # {1, 2, 3, 4, 5}
print(s1.intersection(s2)) # {3}
print(s1.difference(s2))   # {1, 2}
print(s2.difference(s1))   # {4, 5}
print(s1.symmetric_difference(s2)) # {1, 2, 4, 5}


👉 Union, Intersection, Difference – math jaisa hi.

# 5. Subset & Superset
s1 = {1, 2}
s2 = {1, 2, 3}

print(s1.issubset(s2))   # True
print(s2.issuperset(s1)) # True


👉 issubset() / issuperset() relationship check karte hain.

# 6. Disjoint Sets
a = {1, 2}
b = {3, 4}
print(a.isdisjoint(b))  # True


👉 True return karega agar common element nahi hai.

# 7. Set with Immutable Elements

✅ Allowed: Numbers, Strings, Tuples

❌ Not Allowed: Lists, Dictionaries

s = {1, "hello", (2, 3)}   # Valid

# 8. Set Membership
s = {1, 2, 3}
print(2 in s)        # True
print(5 not in s)    # True


👉 Membership test fast hota hai sets me (hashing ke wajah se).

# 9. Length
s = {1, 2, 3, 4}
print(len(s))  # 4


👉 Duplicates count nahi hote.

📝 Quick Use-Cases

# Remove duplicates from list:

nums = [1, 2, 2, 3, 4, 4]
unique = set(nums)   # {1, 2, 3, 4}


Find common elements:

print(set([1,2,3]) & set([2,3,4]))  # {2, 3}


# Check subset/superset:

{1,2}.issubset({1,2,3})   # True
