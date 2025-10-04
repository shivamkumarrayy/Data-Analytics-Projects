## dictiuonary in python 
   dictionary is a collection which is unordered ,changeable and indexed.
  > in python dictionaries are written within curly({}) brackets,and they have keys and values
# create and print dictionary
   dict1={"car":"marauti", "Animal":"Lion" }
   print(dict1)

# Accesing items
 > You can access the items of dictionary by referring to its key name,inside square brackets.
    dict1={"car":"marauti", "Animal":"Lion" }
    print(dict1)
    x=dict1["car"]
    print(x)

# change value in dict
 > you can change the value of specific item by referring to its key name.
 > For Example
    dict1={"car":"marauti", "Animal":"Lion","year":2020 }
     dict1['year']=2021
     print(dict1)
# Adding new element in dict
 >For Example
    dict1={"car":"marauti", "Animal":"Lion","year":2020 }
    print(dict1)
     dict1['Y.O.B']=2021
     print(dict1)
# Loop through a Dictionary
    dict1={"car":"marauti", "Animal":"Lion","year":2020 }
    for x in dict1:
    print(x)
> This will print index values
          OR
  for x in dict1:
 print(dict1[x])
> This will print values

 ## item function to return value of function
       dict1={"car":"marauti", "Animal":"Lion","year":2020 }
       for x,y in dict1.items():
       print(x,y)
  
## Function uses in dictionary
1. len() -- x=len(dict1)
2. pop()
    dict1={"car":"marauti", "Animal":"Lion","year":2020 }
    print(dict1)
    dict1.pop('model')
    print(dict1)
3. update() -- iska use values insert me hota hai     
