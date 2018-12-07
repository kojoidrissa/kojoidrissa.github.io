---
layout: post
title: "PythonDayMX18: Follow Up"
date: 2018-12-05T17:24:24-06:00
update: 2018-12-07T13:24:24-06:00
categories: [conferences, NorAmGT]
---

I spoke at [Python Day Mexico 2018](http://pythonday.mx/) last Saturday. During the Q&A after my talk *(A Junior Developer's Guide to Software Engineering)*, I was NOT satisfied with a couple of answers I gave. And I've thought about them a bit, so here are my updated responses. Hopefully [Maricela](https://twitter.com/mayela0x14) or someone from [PythonDayMX](https://twitter.com/pythondaymx/) will be able to share this with folks who attended my talk.


## Which is better to use, containers or VMs (Virtual Machines)?
One of the things I discuss in my talk is Dependency Management and Deployment. I mentioned 3 technologies but focused mostly on containers and VMs. The question of which is better came up. My answer felt a bit vague and not super useful. 

"It depends on what you're trying to do *(true, but not super helpful)*, containers are more 'lightweight' than VMs *(again, true, but WTF does that even mean?)* and containers are 'the new hotness'".

I think a more useful answer would focus on the main differences between containers and VMs. I'm not gonna be "super-technical" here, but the main difference is a container will (or can) ONLY contain the software needed to run your application. Anything ELSE it needs are supplied by the underlying host OS. A VM, on the other hand, is a LITERAL virutual version of an ENTIRE computer. So, it'll include an OS (and all the software that comes with it), as well as the software you need to run your application. There are [diagrams on the internet](https://www.google.com/search?q=vms+vs+containers&source=lnms&tbm=isch&sa=X&ved=0ahUKEwjWqOnx74nfAhVDhq0KHWWOBwsQ_AUIDigB&biw=1439&bih=798) that show a comparative picture. But in my mind, the key difference is that a container ONLY needs your specific, required software. Yes, there ARE containers that have an OS, but you don't always need those.

So, if you're deploying a simple Python application, with no external libraries, a container for that app could have JUST Python. A VM for the same app would be, basically, a virtual computer (including the OS) that also has Python installed. That's a bit of an oversimplification, but you can see how the 2nd bundle of software is going to be larger or "heavier" or more resource intensive. One as a copy of the OS, one doesn't.

I hope that's helpful. It's not a master class on the topic, but I feel it's more useful than my original answer. The "it depends" part still stands, but I think the extra info on what separates the two items provides more info for deciding what you do or don't need.

## GNU Screen
Another topic was utilities Jr. Devs could benefit from knowing or using. GNU Screen was one of them. Turns out, I'm NOT using it for it's MAIN benefit! I'm using it as a convenient window manager thingy on my local machine so I don't have to add another terminal tab. But one of the MAIN benefits of Screen is for connecting to remote machines (usually via SSH).  So, if you're connected, then use Screen to create another session, if your SSH connection gets disrupted, any processes you had running will still continue. And you can reconnect to that session and after you re-establish your connection. This was much more critical when internet connections were slower and less reliable, but that's still the case sometimes.

There's an excellent article that goes into much more detail about Screen on [Opensource.com](https://opensource.com/article/17/3/introduction-gnu-screen), so I won't go into too much more detail.

## In Conclusion
I may try to provide follow-ups to other talks I give in the future. I always include my [Twitter handle](https://twitter.com/Transition) on my slides, so people can reach out if they want to. But this may be more direct. Especially if **I** want to add to my comments.
