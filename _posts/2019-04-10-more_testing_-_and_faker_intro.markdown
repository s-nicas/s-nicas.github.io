---
layout: post
title:      "More Testing - and Faker Intro..."
date:       2019-04-11 01:03:42 +0000
permalink:  more_testing_-_and_faker_intro
---

I’ve spent the past few weeks talking about testing. It’s because I am quickly becoming obsessed with it!

We broke a major feature to our website recently because someone made a minor change. That change seemed minor at the time -- then ***BAM*** --  we were in a scramble because we couldn’t get things to work. We had no tests for this feature so we didn’t know it was broken until a few days later. Which made it all the more difficult to find. 

If we had tests -- this wouldn’t have happened in the first place. We would have immediately known that our new code had unintended consequences. 

Moral of the story: invest some time upfront by building test and it will save you time in the long run. It took us over 2 days to find the issue! 

Alrighty - moving on to something I learned this week.

I discovered Faker: https://www.npmjs.com/package/faker

Faker generates fake data for you to play with! I’m not very creative and takes me longer to think of a fake name then it will take me to write an entire test -- hence I was excited! Haha :) 

If working in Node.js


To install faker run 

`Npm i faker `


To add faker to your file 

`var faker = require('faker');`

Then you can generate a ton of fake data. 

```
var randomName = faker.name.findName(); // Bobby Blue
var randomEmail = faker.internet.email(); // Scott.Harvey@eri.biz
```

Take care, yall! 

*Build tests - save your future self <3*
