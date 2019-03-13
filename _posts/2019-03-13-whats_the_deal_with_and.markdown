---
layout: post
title:      "What's the deal with == and === ?"
date:       2019-03-13 16:46:20 -0400
permalink:  whats_the_deal_with_and
---


What is the difference between triple equals and double equals? 


Let’s first start off with what they have in common: **both == and === are used for equality comparisons**. 


`7 == 7 // true`
`7 === 7 // true `


**How are they different? **

Double equals also known as lose equality ( `==` ) is used for abstract equality comparison. The main thing to keep in mind is loose equality uses **type conversion**. This means lose equality will compare the two values for equality after converting both values to a common type. 

For example: 

`5 == “5” // true `
 
Double equals converted the ` “5” ` from a string to an integer. Then it is compared for equality and concluded both values are equal and returned true. 

Triple equals or strict equality (`===`) does not perform type conversion. It will immediately compare both values for equality. 

For example: 

`5 === “5” // false `

I hope this helps clear up` ==` vs.` ===` ! 

*Happy coding y’all :) *

