# Object Oriented Programming 
  Classes represent and define concepts, while objects are instances of classes
  
  ***The attributes are the characteristics associated to a type.***

  ***Methods are functions that are part of the class.***
  
  ## Basic Functions
  
  ### dir() function to get all attributes and methods of an object
  
  ### help() function to get the documentation for the corresponding class.
  
  ## Defining a Class
  
      class Apple:
               color="" #attribute
               flavor="" #attribute

      FruitA=Apple()
      FruitA.color="red"
      FruitA.flavor="sour"
      print(FruitA.color) -> red
      
  
  ## Initialize Class Attributes
  
      class Apple:
          def __init__(self,color,flavor):
              self.color = color
              self.flavor = flavor
      
      crimson=Apple("red","sour")
      print("{}, {}".format(crimson.color,crimson.flavor) -> "red, sour"
