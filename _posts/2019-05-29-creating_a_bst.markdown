---
layout: post
title:      "creating a bst"
date:       2019-05-30 02:19:56 +0000
permalink:  creating_a_bst
---


Hi Friends! 

Binary search trees were intimidating to me at first. But once I realized how simple it was to create one -- they became much easier to work with. So today, I will be walking you through just that -- how to create a Binary Search tree from scratch. 

A binary search tree is a combination of binary search trees tied together. A binary search tree consists of a parent node and two child nodes. 

To start off our tree - let's create a BST function

```
function BST(value){
 this.value = value;
 this.left = null;
 this.right = null;
}
```

Great - now we can create a binary search tree!

`let tree = BST.new(4)`



Next, how do we add values to our tree? 

Let’s create an insert method. 

But first a few important facts about a Binary Search Tree. If built correctly: 
* The right node will be greater to the parent node. 
* The left node will always be smaller or equal to the parent node. 
* As the tree progresses - the integer on the right side will continue to grow. 
* As the tree progresses - the integers on the left will continue to get smaller. 

Okay, to add a new value to BST we will use recursion. 

```
BST.prototype.insert = function(value){
 // if value is smaller should go on left
 if(value <= this.value){
 
   if(!this.left) {
     this.left = new BST(value)
   } else {
      // if a node already exist on left then find its place using recursion
      this.left.insert(value)
   }
 }

 else if(value > this.value){
   if(!this.right){
     this.right = new BST(value)
   } else {
     this.right.insert(value)
   }
 }
}
```


And Viola -- we’ve created a new BST and now we can add additonal values to it. 

