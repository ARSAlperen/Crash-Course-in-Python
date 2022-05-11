Lists and tuples are both sequences
# LIST
  ***Mutable***-> which mean members of list can be changed.
  ## Basic Concepts

  ### Search for a value in list

    x=['A','B','C','D']

    'A' in x will return TRUE

  ## Modifying
   ### Append Method (Adding the item to the end of the list
    names=['Ali','Alp','Arslan','İdil','Buğra']
    names.append('Alperen')
  ### Insert Method (Adding the item to the specified index)
    names.insert(0,'Alperen')
    names=['Alperen',"Ali','Alp','Arslan','İdil','Buğra']
  ### Remove Method (Removing the item specified)
    names.remove('Ali')
  ### Pop Method (Popping the item specified by it's index)
    names.pop(3)
  ### Sort Method
  
    list.sort() Sorts the items in the list
  ### Reverse Method
    list.reverse() Reverses the order of items of the list
  ### Clear Method
    list.clear() Removes all the items of the list
  ### Copy Method
    list.copy() Creates a copy of the list
  ### Extend Method
    list.extend(other_list) Appends all the elements of other_list at the end of list  
# TUPLE
  ***Not Mutable***-> which mean members of list can be changed.
  The position of the elements inside the tuple have meaning.
  Tuples can be useful when we need to ensure that an element is in a certain position and will not change.
  
     info=('Alperen','Arslan','male','Ankara) 
     
# ITERATING
 ## Enumerate
 The enumerate() function takes a list as a parameter and returns a tuple for each element in     the list. ***The first value of the tuple is the index and the second value is the element      itself.***
 
    names=['Ali','Alp','Arslan','İdil','Buğra']
    for i,person in enumerate(names): 
       print("{} - {}".format(i+1,person))
       
   Outcome->
   
        1 - Ali
        2 - Alp
        3 - Arslan
        4 - İdil
        5 - Buğra
# COMPREHENSION MORE EASY WAY TO CREATE LIST

Instead of using loops for creating lists comprehension can be used. It is quite powerfull.

    multiple=[x*7 for x in range(1,11)]
    
    multiple=[7,14,21,28,35,42,49,56,63,70]
 
 ## Add Condition
 
    z=[number for number in range(0,100) if number%7==0]
    
 Answer->
 
    [0, 7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98]
