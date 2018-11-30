---
layout: post
title:      "JavaScript Promises "
date:       2018-11-30 03:13:50 +0000
permalink:  javascript_promises
---



What are they? 

I think we can all agree that JavaScript promises have made our coding life a bit easier. But if you were to stop and try to answer the question -- "How does a promise work?" -- it might not be so easy. 

> MDN says the Promise object represents the eventual completion (or failure) of an asynchronous operation, and its resulting value.

A JavaScript promise is just like a promise you might make in real life.  For instance, you promise a child ice cream after dinner. 

Well, we can also create that promise in Javascript.

```
const iceCream = true

const iceCreamPromise = new Promise(function(resolve, reject){
  if (iceCream){
    resolve("Happy Kid")
    } else {
    reject("Sad Kid")
  }
})

const whatHappened = function () {
  iceCreamPromise
  .then(function(success){
    console.log(success)
  })
  .catch(function(error){
    console.log(error)
  })
}
```




A promise has 3 states:

 **Pending** is the initial state. The promise is in progress -- neither rejected nor fulfilled.
 **Fulfilled** means the promise was successful.
 **Rejected** means the promise was unsuccessful.

Okay, let's run our handy function of whatHappened() to see if the kid got his ice cream.

whatHappened()  *currently in the pending state*
//Happy Kid             * fulfilled*


Woohoo! Successful! The kid got his ice cream.

Once our whatHappened() function was successful, our `.then()` function received its value.

What is .`then()`?

`.then()` is available on the Promise instance object. The` .then() `function is called with whatever the return value of the promise is. Neat note: ` .then() `is a promise itself. If the `.then()` is successful, the promise will resolve.

Since `.then()` is a promise, we can chain another promise to it: `.catch()`

`.catch()` only deals with rejected cases. 

Here is one way to think about it: We create a promise. If the promise is successful, `.then() `will process the results. If the promise is unsuccessful, `.then()` will throw out the response. Lucky for us, `.catch()` is ready to catch it. 


If you're thinking callbacks right now, you're right.

> Here is MDN  - Essentially, a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.

It's likely you have seen ` .then()` before you’ve seen` new Promise(`). That's because we are taking advantage of already created promises.

Yup! A modern function returns a promise object, which is why we have been able to chain `.then()` to it.

Promises is what makes asynchronous operations fairly easy. We can chain multiple promises together.

This example has been very helpful for me -** by MDN. **

```
doSomething()
.then(result => doSomethingElse(result))
.then(newResult => doThirdThing(newResult))
.then(finalResult => {
  console.log(`Got the final result: ${finalResult}`);
})
.catch(failureCallback);
```

Each promise represents the completion of another asynchronous step in the chain. They will be completed in order and each will wait for its turn before running. 

After DoSomething runs, the value will be passed to doSomethingElse as result. When doSomethingElse is done, it will pass the new value to doThirdThing as newResult and so forth. 


 Lots of info here. Thanks for sticking with me. Send me a note if you have any questions or feedback! 


