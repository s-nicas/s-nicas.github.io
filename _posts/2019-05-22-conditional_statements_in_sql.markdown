---
layout: post
title:      "Conditional statements in SQL"
date:       2019-05-23 01:30:36 +0000
permalink:  conditional_statements_in_sql
---


I recently had to do a SQL query but I only needed results that met a certain condition. I was thrilled when I found SQL has case statements. They are similar to else/if statements. 

Here is an example: 

```
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

This can be added in any area of your query. 

Lets say you are querying your pets database. If a cat is small return "Small Kittens" else return "Large Kittens". 

```
SELECT size,
CASE
    WHEN size = "small" THEN "Small Kittens"
    WHEN size =  "large" THEN  "Large Kittens"
    ELSE "Normal Size Kittens"
END 
FROM Cats;
```

Pretty cool! 



