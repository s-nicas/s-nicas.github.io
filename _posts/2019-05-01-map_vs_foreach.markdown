---
layout: post
title:      "Map vs. ForEach	"
date:       2019-05-01 06:43:21 +0000
permalink:  map_vs_foreach
---


Today, I’m revisiting two of my favorite methods map and ForEach. Both methods are fairly similar and sometimes they can be easy to get confused. 

The ForEach method executes a provided function once for each array element.

for example 

```
let array = [1,2,3,4]

array.forEach(num => console.log(num + 1))

// 2
// 3
// 4
// 5
```

The map() method creates a new array with the results of calling a provided function on every element in the original array.

For example 

```
let array2 = [1,2,3,4]

array2.map(num => num +1 )

//  [2,3,4,5] 
```


As you can see the main difference is map will create a new array. Yet forEach will just run the function on each value. 







