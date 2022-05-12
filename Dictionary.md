# Dictionary

***Use dictionaries when you plan on searching for a specific element.***

 ## Operations

    toc = {"Introduction":1, "Chapter 1":4, "Chapter 2":11, "Chapter 3":25, "Chapter 4":30}
  ### Add New Item
    toc["Epilogue"]=39
  
  ### Change Item Value
  
    toc["Chapter 3"]=24
  ### Check if Item Exist
    print("Chapter 5" in toc)

  ### Delete Item
     del toc["Chapter 4"]
     
 ## Methods and Iterating
 
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
      
   ### Real Use of Dict
   
    def count_letters(text):
     result={}
     text=text.upper()
     for letter in text:
         if letter!=" ":
          if letter not in result:
           result[letter]=0
          result[letter]+=1
     return result

    count_letters("One Day I Will Work as a Data Scientist")
     
   -> Outcome
   
    {'O': 2,
    'N': 2,
    'E': 2,
    'D': 2,
    'A': 5,
    'Y': 1,
    'I': 4,
    'W': 2,
    'L': 2,
    'R': 1,
    'K': 1,
    'S': 3,
    'T': 3,
    'C': 1}
    
    
   ### Using Dict with Lists
   
   -> Question
   
    wardrobe = {"shirt":["red","blue","white"], "jeans":["blue","black"]}
    for items,values in wardrobe.items():
     for i in range(len(values)):
      print("{} {}".format(values[i],items))
      
   -> Answer

    red shirt
    blue shirt
    white shirt
    blue jeans
    black jeans


# Change Keys to Items and Items to Keys

    def groups_per_user(group_dictionary):
     user_groups = {}
     # Go through group_dictionary
     for keys,users in group_dictionary.items():
      # Now go through the users in the group
      for user in users:
       if user not in user_groups:
        user_groups[user] = []
       user_groups[user].append(keys)

     return(user_groups)
     
     print(groups_per_user({"local": ["admin", "userA"],
    "public":  ["admin", "userB"],
    "administrator": ["admin"] }))
    
  -> Outcome
  
    {'admin': ['local', 'public', 'administrator'], 'userA': ['local'], 'userB': ['public']}
