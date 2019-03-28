---
layout: post
title:      "What is continuous integration? "
date:       2019-03-28 00:56:48 +0000
permalink:  what_is_continuous_integration
---


Continuous integration is the practice of merging changes into a master multiple times per day. Each merge will be a small change and a very specific change. 

Each merge is verified by an automated system. Which automatically runs your code and checks it for issues. 

What problem does continuous integration fix? 

**Save Time**

Merging multiple times per day - avoids the “monster merge”. When a merge has big changes, and you are working in a team those changes can have unintended consequences. For one - it can be difficult to merge with others code - especially if that code has yet to be merged. 

This can be counter productive. A teammate may have to go back an rework their own code because - well - code has literally changed right under them. 

**Avoid Bugs**

When merging a large change, it can quickly introduce bugs. Those bugs can be difficult to find as there is a lot of code to go through. 


**Ensures it works **

Before merging you set up an automated system to run test on the new code and ensure it won’t create any issues. Ensure is a strong word -- but it minimizes the risks of unintended bugs. I was introduced to CircleCI https://circleci.com/  this week. Works great :) 

