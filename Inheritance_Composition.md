# Inheritance (Father and Son Relationship)

Below example Shirt class inherit from Clothing class and can use all methods and attributes of Clothing class.

    class Clothing:
      material = ""
      def __init__(self,name):
        self.name = name
      def checkmaterial(self):
        print("This {} is made of {}".format(self.name,self.material))

    class Shirt(Clothing): -> Shirt 
      material="Cotton"

    polo = Shirt("Polo")
    polo.checkmaterial()
