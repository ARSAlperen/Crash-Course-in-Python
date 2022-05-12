# Dictionary

 ## Basics

    toc = {"Introduction":1, "Chapter 1":4, "Chapter 2":11, "Chapter 3":25, "Chapter 4":30}
  ### Add New Item
    toc["Epilogue"]=39
  
  ### Change Item Value
  
    toc["Chapter 3"]=24
  ### Check if Item Exist
    print("Chapter 5" in toc)

  ### Delete Item
     del toc["Chapter 4"]
     
 ## Iterating
 
     for items in toc:
      print(items)
 
 Input->   
 
    for items,amount in toc.items():
      print("{} have {}".format(items,amount))

  Output->
    
    Introduction have 1
    Chapter 1 have 4
    Chapter 2 have 11
    Chapter 3 have 25
    Chapter 4 have 30

  ### Getting Key Values
      
      toc.keys() = dict_keys(['Introduction', 'Chapter 1', 'Chapter 2', 'Chapter 3', 'Chapter 4'])
  
  ### Getting Values

      toc.values() = dict_values([1, 4, 11, 25, 30])
