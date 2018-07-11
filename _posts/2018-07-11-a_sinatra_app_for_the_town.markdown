---
layout: post
title:      "A Sinatra app for The Town! "
date:       2018-07-11 16:04:57 +0000
permalink:  a_sinatra_app_for_the_town
---


 
Coming up with a concept for the Sinatra project was easy: I built something my community actually needs. 

I’m currently a resident of Oakland, California. I often feel Oakland is under the radar. While that’s great for me — bars and hiking trails are rarely crowded— it’s disheartening when I hear others criticizing the city because there’s not enough to do. There is so much to enjoy in Oakland — if you know where to look. So I created an application that could feature all the neat events Oakland has to offer. 

My sinatra application has two models: a user model and an event model. A user has_many events. An event belongs_to a user. A user can create, edit and delete their event postings. Yet, all events are visible to all users. 

It’s basic, but I consider this a starting point. I hope to add additional features, such as RSVPs, maps, directions, profile pictures and, of course, jazzing it up with some neat styling. 

But first, the foundation! Without a simple, clean and strong working foundation, add-on features would be a mess. 

My submission:  

I used RESTful principles for my routes and actions, which I have learned to enjoy. Thank you, Roy Thomas Fielding, for organizing the internet. (Well, at least the URLs.) I’m fascinated with them now! 


To keep my URLs looking fresh, I used slugs too. Who-wants-to-see-event-ids-when-they-can-see-the-name!


Active Record Validations were used to ensure users complete forms and my program isn’t jammed with empty strings. I found this incredibly useful; full blog post coming soon!


 I used Flash[:messages] to alert users when they are trying to do something they can’t, such as editing another user’s event or viewing events without logging in first. Users have to sign up to see what’s happening in Oakland :)
 
Lastly, to protect users’ passwords, I used the 'bcrypt' gem. 

Feel free to check it out if you’re curious. I'm always learning, so shoot me a note if you have any feedback. [https://github.com/s-nicas/underground-oakland]

Happy coding! 
