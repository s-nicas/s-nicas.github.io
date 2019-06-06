---
layout: post
title:      "Splice it up"
date:       2019-06-06 01:25:36 +0000
permalink:  splice_it_up
---


Javascript arrays have a handy prototype method called splice. 


Splice changes an array by deleting or adding items into an array. Which comes very handy! 
Splice takes in 3 arguments. 

**start**
The first argument is start and it is required. Start represents the index in which we should start to alter the array. 

**deleteCount **

Delete count is an optional argument. It should be the number of elements that should be deleted from the start index. 

**toAdd**

The last argument or series of arguments are the items that should be added into the array. 


*With splice you can add an item, while deleting another which can be very handy! *


Keep in mind - If you do not specify any elements, splice() will only remove elements from the array.


You can add an item like this: 

```
var fruits = ['Apples', 'Oranges', 'Pears’];
fruits.splice(1, 0, 'Bananas');
// inserts at index 1 and deletes 0 items 
console.log(fruits);
// expected output: ['Apples', ‘Bananans’, 'Oranges', 'Pears']
```

Super neat! 


