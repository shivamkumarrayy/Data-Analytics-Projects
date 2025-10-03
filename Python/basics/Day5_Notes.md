# Q. What is List ?
Ans: List is a collection of different or similar types of values and different types of  items./ or store multiple types of values in a single unit.
 >  The item in the list is seperated by comma ( , ) or enclosed within  brackets ( [] ).
  e.g. a=["Ram", 1,2,3]
### print(a)
#Output = ["Ram", 1,2,3]

# PROPERTIES
  > List is mutable and in ordered.- mutable means we can change the value when list is created

## LLIST OPERATIONS ( Indexing ,Slicing)
> Indexing - stare with 0 to ( n-1 ) this is called forward indexing.
  from given example , a[0] - "Ram", a[3] = 3;
> Backward indexing start with the toal number of elements and ends with -1 not 0.
  from example a [-4 ]= "Ram" ,a[ -1] = 3;

> Slicing is the process that  allows you to extract specific portions of sequences like lists, tuples, and strings
 > syntax of Slicing [ Start : End : Step]

  e.g. 
my_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
# Basic slice: elements from index 2 up to (but not including) index 5
print(my_list[2:5])    # Output: [2, 3, 4]

# Slice from the beginning to a specific index
print(my_list[:5])     # Output: [0, 1, 2, 3, 4]

# Slice from a specific index to the end
print(my_list[7:])     # Output: [7, 8, 9]

# Slice with a step
print(my_list[0:10:2]) # Output: [0, 2, 4, 6, 8] (every other element)

# Reversing a sequence using slicing
print(my_list[::-1])   # Output: [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]

# Negative indexing in slicing
print(my_list[-6:-1]) # Output: 4,5,6,7,8  (from the 6th character from the end up to the last)

####
 COMMON LIST METHOD(append(), extend(), insert(), remove(), pop(), sort(), reverse() )
> The append() method in Python lists is used to add a single element to the end of an existing list. This method modifies the original list in place, meaning it does not create a new list but rather updates the one it's called upon. 
  Syntax:
        list_name.append(element)
    my_list = [1, 2, 3]
print(f"Original list: {my_list}")

# Append a single number
my_list.append(4)
print(f"After appending 4: {my_list}")
--- Output: After appending 4: [1, 2, 3, 4]

# Append another list (as a single element)
another_list = ['a', 'b']
my_list.append(another_list)
print(f"After appending another_list: {my_list}")
--- Output: After appending another_list: [1, 2, 3, , ['a', 'b']]


>> extend()
The extend() method in Python lists is used to add all the elements of an iterable (like another list, tuple, set, or string) to the end of the current list. It modifies the original list in place, meaning it does not create a new list but rather expands the existing one. The extend() method returns None.
Syntax:
   list.extend(iterable)
# Extending a list with another list
my_list = [1, 2, 3]
another_list = [4, 5, 6]
my_list.extend(another_list)
print(my_list)
--- Output: [1, 2, 3, 4, 5, 6]

>>> insert()
The insert() method in Python lists is used to add an element at a specific position (index) within the list. It modifies the list in place and does not return a new list.
Syntax:
    list.insert(index, element)
# EXAMPLE
my_list = ["apple", "banana", "cherry"]
# Insert at a specific index
my_list.insert(1, "orange")
print(my_list)
--- Output:['apple', 'orange', 'banana', 'cherry']

# Insert at the beginning (index 0)
my_list.insert(0, "grape")
print(my_list)
--- Output: ['grape', 'apple', 'orange', 'banana', 'cherry']

# Insert at an index beyond the current length (appends to the end)
my_list.insert(10, "kiwi")
print(my_list)
--- Output: ['grape', 'apple', 'orange', 'banana', 'cherry', 'kiwi']

# Insert using a negative index
my_list.insert(-2, "mango")
print(my_list)
--- Output:['grape', 'apple', 'orange', 'mango', 'banana', 'cherry', 'kiwi']


>>> remove()
The remove() method in Python lists is used to remove the first occurrence of a specified value from the list. 
Syntax:
list_name.remove(value)
. value - jis item ko hatna ho 
Example:
my_list = [1, 2, 3, 2, 4, 5]
my_list.remove(2)
print(my_list)
Output: [1, 3, 2, 4, 5]

>>> pop()
The pop() method removes the element at the specified position.

Syntax:
     list.pop(pos)
Example:
Remove the second element of the fruit list:
fruits = ['apple', 'banana', 'cherry']
fruits.pop(1)
---Output:['apple',  'cherry']
Example
Return the removed element:
fruits = ['apple', 'banana', 'cherry']
x = fruits.pop(1)
---Output:banana

>>>sort()
method that will sort the list alphanumerically, ascending, by default:

Example
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)
---Output: ['banana', 'kiwi', 'mango', 'orange', 'pineapple']

To sort descending, use the keyword argument 'reverse = True':
Example
Sort the list descending:
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist)
---Output:['pineapple', 'orange', 'mango', 'kiwi', 'banana']

>>> reverse()
The reverse() method reverses the sorting order of the elements.
Syntax:
   list.reverse()
my_list = [1, 2, 3, 4, 5]
print(f"Original list: {my_list}")
my_list.reverse() # Reverses the list in place
print(f"Reversed list: {my_list}")
--- Output:Original list: [1, 2, 3, 4, 5]
           Reversed list: [5, 4, 3, 2, 1]

>>> Iterating through a List (for loop)
my_list = ["apple", "banana", "cherry"]
for item in my_list:
    print(item)
-- my_list = ["apple", "banana", "cherry"]
for i in range(len(my_list)):
    print(f"Element at index {i}: {my_list[i]}")

--my_list = ["apple", "banana", "cherry"]
for index, value in enumerate(my_list):
    print(f"Index: {index}, Value: {value}")

>>nested list
m = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
odds = []

for r in m:
    for e in r:
        if e % 2 != 0:       # Check if element is odd
            odds.append(e)
print(odds)
---output: [1, 3, 5, 7, 9]

>>>> TUPLES
   A Tuple is a collection which is ordered and unchangeable.
>  it is declared as
      tuple1= ("1,2,"shiv","raj")
> Tuple is immutable
> Occupy less space than list
>  takes less time to execute than list
>>>> Creating tuple
>    Using tuple display construct
    tuple1 = ()
    tuple2= (var1,var2..)
>  Creating single element tuple
      tuple1(1,)
 # Creating tuple from string
   t1 =tuple('world')
   >> t1
>> ('w','o','r','l','d')

# Creating from list
list1 = [1,2,3,4,5]
t1=tuple(list1)
>> t1
  (1.2.3.4.5)
#  Traversing tuples
  t1=(1,2,3,4,5)
   for i in t1
    print(i)
>  or for i in range(len(t1)):
     print(t1[i])
# Joining of tuples
  t2 = (1,2,3)
  t3= (4,5,6)
  t4 = t2 + t3
  print(t4)
# Repeating of tuples
t1=(1,2,3)
t2=t1*3
print(t2)
-- output : (1,2,3,1,2,3,1,2,3)
# Slicing the tuples
The syntax is:
T = [start;stop:step]
>> Example:
  tuple1 = (12,13,14,15,16,17)
  t2= tuple1[0:5:2]
>> print(t2)
 -- output:(12,14,16)
   


































