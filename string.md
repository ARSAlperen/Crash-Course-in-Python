---
title: "Python String"
author: "Alperen Arslan"
---

# Operations
  ## len
```   
  len("Zeynep")=6
``` 
  ## Index operations
``` 
  fruit = "Mangosteen"
  
    fruit[1:4] ='ang'
    fruit[:5] = 'Mango'
    fruit[5:] = 'steen'
    fruit[:5] + fruit[5:] = 'Mangosteen'

  animal="lions tigers and bears"
  
    animals.index("g")=8
    animals.index("bears") =17
``` 
  ## Check if substring is in String

    "tigers" in animals=True
    "dragons" in animals=False

# Methods

  ## .upper(), .lower()
    country="turkey"
    country.upper()="TURKEY"

  ## strip()
    name=" Alperen  "
    name.strip()="Alperen"
     ## lstrip() and rstrip() are good options as well.

  ## count()
    name.count("e")=2

  ## endswith()
    name.endswith("ren")= True

  ## isnumeric()
    name.isnumeric() = False
    s="2"
    s.isnumeric() = ***True***

  ## split() and join()
```{r}
  name.split("e")= ['Alp', 'r', 'n']
  " ".join(["This","is","a","sentence"])=This is a sentence".
``` 
  ## replace()
    name.replace("e","@")= "Alp@r@n"

# Formatting {} 
```{r}
  name="Alperen"
  surname="Arslan"
  program="Python"
``` 
  "Hi, I'm {name} {surname}. Trying to learn {program}".format(name=name,surname=surname,program=program) 
  ->"Hi, I'm Alperen Arslan. Trying to learn Python"
  
  ![image](https://user-images.githubusercontent.com/105153770/167711334-ac0db737-eeb8-4ecf-b9c9-098b14c5dbe4.png)
