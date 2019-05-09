---
layout: post
title:      "How to flatten an array"
date:       2019-05-09 00:13:08 +0000
permalink:  how_to_flatten_an_array
---

```
flat()
```

Flat is an array method. It creates a new array with all sub-arrays concatenated together -- up to a specific depth. Basically, flat() can help you get out of a messy nested array. 

Example 

```
var numberArray = [5, 6, 7, [10, 9]]

numberArray.flat(); 

// [5, 6, 7, 10, 9]

```

It concatenated the nested array into one clean looking array. 

What happened to numberArray? Let’s call it


```

numberArray

//  [5, 6, 7, [10, 9]]

```

numberArray remains unchanged. Flat() is non-destructive it will create a new array and leave the original one untouched. So remember, if you need to retrieve our flattened array at a later time it is best to save it in a new variable. 



```

var numberArray = [5, 6, 7, [10, 9]]

var flatNumberArray = numberArray.flat(); 

```

Now let's call them one more time. 

```

numberArray

//  [5, 6, 7, [10, 9]]

flatNumberArray

// [5, 6, 7, 10, 9]

```


Now we can reference both arrays in the future!


Flat takes in one argument - **depth**. Let’s explore it a bit! 

`arr.flat([depth]); `

**Depth** is an optional argument. It specifies how deep it should flatten an array. The default of depth is 1. 

`var nestedNumberArray = [1, 2, 3, [4, [9,10]]]`


How deep do we need to go to get an unnested array? 



Answer: 2

```

var unnestedArray = nestedNumberArray.flat(2)

unnestedArray 

// [1,2, 3, 4, 9, 10]

```

Neat!


Thanks for sticking with me here --- happy coding! 

Sonia 

