---
layout: post
title:      "JavaScript Functions"
date:       2018-10-22 16:18:31 -0400
permalink:  javascript_functions
---


Today I want to spend some time on Javascript functions, the language’s fundamental building blocks. 

Functions perform tasks and calculate values, while also organizing your code and making it readable. Can you envision a world without functions? Programs would look like a huge run-on sentence -- statements upon statements with no organization. Ahhh -- I don’t even want to think about the debugging process. Thank you functions for keeping me sane! 

Defining a function 

We can define functions in a few different ways in Javascript. 

```
function greeting(name) {
	return `Hello ${name}`
}
```

**Function Declaration **

Above is a basic example of a function declaration. Let's work our way through this function from left to right. 

* Function declarations are defined with the keyword function.  
* Next is the name of the function. In the example above, greeting is the name of the function. 
* The set of parentheses () holds our parameters.
* The curly brackets {} encloses our statements. Our statement is the code that will be executed once the function is evoked. 
* Function declarations are also known as **function statements**. 
* Function declarations are hoisted. Meaning you can call the function before it is defined. 

That’s it for function declarations. Simple enough!

Before moving forward, how do we invoke a function? 

**Invoking a function**

As I mentioned earlier, our function has to be invoked in order for the code to executed. This process is also called “call a function” or “execute a function.” I will be sticking to invoke in this blog. 

If we want to invoke our greeting function we would do so like this:

```
function greeting(name) {
	return `Hello ${name}`
}

greeting('Sonia')

```



Let’s walk through the above. 

We invoke a function by
1. Stating the name of the function.
1. Followed by parenthesis () Our parenthesis will hold our arguments. In this example my argument is my name: Sonia. 

That’s it! Once our function is invoked our program will return 

```
"Hello Sonia"
```

This brings up another important concept that I want to touch on before I return to other types of functions. 



**Arguments & Parameters**
 
I’ve heard many people use these two concepts interchangeably -- but they shouldn’t. They are two different terms.  

Parameters are variables in functions, while arguments are the actual values passed into the function when invoking the function.

In our greeting function example, **name** is my parameter, while **Sonia** is my argument. 

Here is a quick visual:

```
function name(parameters){
  statements
}

//to invoke a function

name(arguments)
```



*Okay, back to defining functions! *




**Function Expressions **

Let’s convert my example function declaration **greeting()** to a function expression. 

```
var greeting = function(name){
  return `Hello ${name}`
}	
```


* A function expression is a function defined and stored as the value of a variable. 
* Another thing that should stand out in the above example is the function has no name. It is an anonymous function! 
* Function expressions can be named. However, the name would only be accessible within the body of the function scope. It cannot be accessed outside of the function. 
* Function expressions are not hoisted, meaning they cannot be called before they are defined. 

* To invoke our function expression we would do so like this:
```
greeting("Sonia")
```


* Another neat thing about function expression is it can run as soon as it is defined. This is known as IIFE, which stands for Immediately Invoked Function Expression. 

For example 
```
var timesTwo = function(){
  return 2*2
}()

// Immediately creates the output: 

timesTwo; // 4
```


* Lastly function expressions can be passed in as an argument to another function. A function inside a function --- dang! You have probably used a function expression inside another function without even knowing it. These types of functions are called Higher Order Functions. An example of a higher order function is the filter method in Javascript. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter




**Arrow Functions **

```
var greeting = (name)=>{return `Hello ${name}`}
```

Or we can also write it like this: 
```
var greeting = (name) => `Hello ${name}`}
```



* Arrow functions is another way to write Function Expressions.
* Arrow functions replaces the word function with an arrow =>. The arrow follows the parameters. 
* The two examples above do the same thing. When there is only one parameter i.e. name, the parentheses around the parameter list can be omitted.  
* If the body is a single statement versus a block, the expression will be automatically returned without using the keyword return. The curly brackets can also be omitted. 


Phew! That was a lot of information. Thanks for sticking with it and shoot me a note if you have any questions. 

Happy coding! 
