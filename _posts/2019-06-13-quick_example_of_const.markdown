---
layout: post
title:      "Quick example of const "
date:       2019-06-13 02:16:38 -0400
permalink:  quick_example_of_const
---


When a variable is declared with const it is mutable but it cannot be reassigned. So when can you use it and how?


**This is allowed**

```
const count = 0

count++
```

We are changing the value of count but we are not reassinging it. 

**This is not allowed **

```
const counter  = 0

count = count + 1
```

Here wer are trying to reassing count and thus it is not allowed. 




