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
    
# TUPLE
  ***Not Mutable***-> which mean members of list can be changed.
  The position of the elements inside the tuple have meaning.
  Tuples can be useful when we need to ensure that an element is in a certain position and will not change.
  
     info=('Alperen','Arslan','male','Ankara) 
     
# ITERATING
 ## Enumerate
 
    names=['Ali','Alp','Arslan','İdil','Buğra']
    for index,person in enumerate(names):
       print("{} - {}".format(index+1,person))
       
   Outcome->
   1 - Ali
   2 - Alp
   3 - Arslan
   4 - İdil
   5 - Buğra
   
