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

