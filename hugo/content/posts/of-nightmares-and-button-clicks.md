---
title: Of Nightmares and Button Clicks
date: 2018-05-24 12:48:07 -0400
author: Lance Akins

---
I had a seemingly simple task of fixing a submit button that was allowing multiple submissions on one of our ASP.NET Web Forms sites. Getting the client and server to agree on when to disable the button proved problematic. I spent a few hours combined with a couple of more experienced developers on our team, and even tried to implement a similar solution from one of our other sites. I was stumped. The pressure was mounting. I got an idea, stayed late, and got it to work by wrapping a div container around the button, writing a JavaScript function that declares variables initialized to ClientID of their corresponding Regular Expression Validator, and used an if( var1.isvalid && var2.isvalid && ...) statement to hide the div. Finally I added a progress updater below the button and set the button's onClientClick to return JavaScript function. It worked beautifully. The next day I updated the email recipient for when someone submits that form to a valid email address, and since the email no longer failed to send, it no longer hits the catch block. Now the form is replaced with a thank you message as soon as you submit, making my changes unnecessary.