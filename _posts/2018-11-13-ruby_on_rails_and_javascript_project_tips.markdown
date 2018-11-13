---
layout: post
title:      "Ruby On Rails & JavaScript project tips "
date:       2018-11-13 07:45:12 +0000
permalink:  ruby_on_rails_and_javascript_project_tips
---



Here are a couple of ah - ha moments I had while working on my Javascript & Rails project. I hope I can save you sometime and stress while you work on your project. 

# Javascript files aren't working?

Here are a few tips on how to troubleshoot.

Ensure the newly created file is included in your JavaScript manifest file.  

 `//= require your-file-name`


*side note*   //=. This is called a directive, and it tells sprockets that this isn't a normal JS comment.

Once you checked your manifest file. Ensure you loaded it in your application. You will do so in your apps layout file 

```
<%= javascript_include_tag "application" %>
```

Still not working? 

If you started writting code in your javascript file. Wait! Don't. Write. Anymore. Code! 

Before writing any code - always pause and ensure your JS file is working correctly.  


Here is a quick tip I learned. If you started writting code - comment it all out. 

*  Create an alert inside your JS file

```
$(document).ready(function(){

     alert('Hello from your JS file')

}
```

*  Run your application
*  If you recieve an alert - your file is set up correctly. YAY! Now you know the issue is with your code and not with the file. 

Testing your code and files as you build your project can save you time. You can immediately hone in on the problematic code or file. 

If you don’t test your code as you go - figuring out where the issue is coming from can be a huge time suck. 




# Ajax post request isn’t working?

Turbolinks could be the culprit. 
If you are receiving the following message in your console 

```
Turbolinks.clearCache()
Turbolinks.visit("http://localhost:3000/some_new_page", {"action":"replace"})
```

You can confidently blame turbolinks. 

Turbolinks gives applications a performance boost. It does so by hijacking certain events and reloading pages using the History API. This can interfere with AJAX requests. 

There are several solutions for this. My application is fairly simple. The performance boost that Turbolinks provided appeared to be nominal. So I removed the gem and deleted it from my JavaScript manifest file. This solution should work for most projects. 

If you feel Turbolinks is beneficial to your application take the time to understand how it works and how it will impact your application. Otherwise you may run into several unexpected issues. To learn more about Turbolinks https://github.com/turbolinks/turbolinks. Used correctly - turbolinks can a helpful tool! 

Good luck!! 

