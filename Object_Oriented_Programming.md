# Object Oriented Programming 
  Classes represent and define concepts, while objects are instances of classes
  
  ***The attributes are the characteristics associated to a type.***

  ***Methods are functions that are part of the class.***
  
__Classes and Instances__
- Classes define the behavior of all instances of a specific class.

- Each variable of a specific class is an instance or object.

- Objects can have attributes, which store information about the object.

- You can make objects do work by calling their methods.

- The first parameter of the methods (self) represents the current instance.

- Methods are just like functions, but they can only be used through a class.
  
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
      
  ## Special Methods
  
  ***Special methods***
  
   - Special methods start and end with __
   - Special methods have specific names, like __init__ for the constructor or __str__ for the conversion to string.
  ## __init__ Initialize Class Attributes (Constructors)
  
      class Apple:
          def __init__(self,color,flavor):
              self.color = color
              self.flavor = flavor
      
      crimson=Apple("red","sour")
      print("{}, {}".format(crimson.color,crimson.flavor) -> "red, sour"
      
      
      class Person:
      def __init__(self, name):
          self.name = name
      def greeting(self):
          # Should return "hi, my name is " followed by the name of the Person.
          return "hi, my name is {}".format(self.name) 

      some_person = Person("Alperen")
      print(some_person.greeting())

 ## __str__ Method to set a string for class
 
  ***print a friendly message instead of a bunch of numbers.***
 
      class Apple:
          def __init__(self,color,flavor):
              self.color = color
              self.flavor = flavor
          def__str__(self):
              return "This apple is {} and its flavor is {}.".format(self.color,self.flavor)
      
      crimson=Apple("red","sour")
      print(crimson) -> This apple is red its flavor is sour.
      
  ## Dockstring -> Adding own help documentation to functions, classes, and methods
  
  To add dockstring to a function, a class or a method need to write """ """ string at the beginning of the code
  
    class Person:
       """ Give necessary information about the person who is working at X company."""
       "Dockstring is the line above " 
       age=0
       name=""
       surname=""
     
       def intro(self):
          "Outputs a message including the name of the person."""
          "Dockstring is the line above " 
          print("Hi, I'm {} {}.".format(self.name,self.surname)
 
 The dockstrings will appear when help(Person) typed.
      
  
      
  
