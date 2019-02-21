---
layout: post
title:      "The many ways of if and else statements - Javascript"
date:       2019-02-21 01:09:48 +0000
permalink:  the_many_ways_of_if_and_else_statements_-_javascript
---


Conditional statements are important pieces of code. They make decisions and carry out actions depending on an input.

Here are a few different ways you can write these statement in Javascript.

Lets say we want to write a conditional statement for a stop light, in pseudocode it would look something like this:


```
if(red){
  return stop
} else if (green){
  return go
} else {
  return slow
}
```



Our conditional statement will run in order. Lets break down what happens:  

* If the stop light is red the conditional statement will return stop and we will exit the statement. 
* If the stop light is not red it we will move on to the next condition. 
* Next if the stop light is green it will return go and will exit the statement. 
* If the stop light is not green it will move on to the next condition. 
* If all other conditions are not met our last condition is an else statement - it will run and it will return slow. 

Now let's say we want all drivers to be extra cautious and we want them to stop at both red and yellow lights. 

Our function in pseudocode would look something like this: 

```
if(green){
  return go
} else {
  return stop
}
```



Great - now we only have two conditions. We can refactor this code further: 

```
if (green){
  return go
} 
return stop
```



You don’t have to include the else statement and the second pair of curly brackets. This works because if the light is not green it will not return and the function will keep moving until it does find a return statement. The final return is not part of the conditional statement. 


Furthermore this can also be written like this: 

```
if(green) return go 

	return stop 
```

The curly brackets can be omitted. This is okay when you only have one condition. It looks clean and simple. However I would caution you when omitting the curly brackets if you have multiple conditions like so: 

```
if(green) return go 
else if(red) return stop 
else return slow 
```


Take a second to think why the above can get messy? 


When you have several lines of code it can be difficult to read the above. The curly brackets gives us spacing and it’s makes the code easier to follow. 

Lastly, if we only have one condition - it’s a good opportunity to use the ternary operator. 

```
(green) ? go : stop 
```

Here is one more example in clearer pseudocode using the ternary operator. 

```
(condition) ? if met run this code : else run this 
```

That wraps different types of conditional statements. 

Happy coding! 


