---
layout: post
title:      "Asynchronous vs. Synchronous"
date:       2019-03-20 21:13:44 +0000
permalink:  asynchronous_vs_synchronous
---




*What’s the difference? *


**Synchronous**

Synchronous means code is run in order - starting from the top and moving it’s way down. 

```
console.log(‘Green’)
console.log(‘Red’)
console.log(‘Yellow’)
```

This will output 

```
Green 
Red
Yellow
```

Synchronous operations are blocking which means only one operation can be in progress at a time. 

Our second console.log will not start until our first console.log starts. 

**Asynchronous**

Asynchronous, is a multitasker, it allows multiple things to happen at the same time. It does not block other code from running. If it comes across code that requires blocking, it starts it, and it keeps moving without blocking for the result. When the action finishes the program gets informed and gets access to the results. 

```
console.log(‘Green’)
setTimeout(() => console.log(‘Red’), 500);
console.log(‘Yellow’)
```

This will output 

```
Green
Yellow


Red
```

Our program will keep running even though our second console.log had a timeout set. Once the timeout runs out - it will console.log red - which is why it comes last. Pretty cool!

