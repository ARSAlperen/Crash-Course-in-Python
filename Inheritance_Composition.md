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

# Composition

***You can have a situation where two different classes are related, but there is no inheritance going on. This is referred to as composition -- where one class makes use of code contained in another class. ***

    class Clothing:
      stock={ 'name': [],'material' :[], 'amount':[]}
      def __init__(self,name):
        material = ""
        self.name = name
      def add_item(self, name, material, amount):
        Clothing.stock['name'].append(self.name)
        Clothing.stock['material'].append(self.material)
        Clothing.stock['amount'].append(amount)
      def Stock_by_Material(self, material):
        count=0
        n=0
        for item in Clothing.stock['material']:
          if item == material:
            count += Clothing.stock['amount'][n]
            n+=1
        return count

    class shirt(Clothing):
      material="Cotton"
    class pants(Clothing):
      material="Cotton"

    polo = shirt("Polo")
    sweatpants = pants("Sweatpants")
    polo.add_item(polo.name, polo.material, 4)
    sweatpants.add_item(sweatpants.name, sweatpants.material, 6)
    current_stock = polo.Stock_by_Material("Cotton")
