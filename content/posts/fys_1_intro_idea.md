---
date: "2019-04-20T00:07:40+01:00"
title: "FyS : introduction and idea"
tags:
  - "freeyoursoul story"
  
draft: true
---

# FyS : introduction and idea

## What is FreeYourSoul concept, where did the idea come from ?


Basically, the idea was just to have a big project, that would force me to cover and explore multiple subjects into depth, and to improve in a lot of different aspect of software engineering and in the C++ language itself.
The project began in late 2017, and I wanted to try the new features of the C++ standard. The only important thing I wanted for my project was to be performance sensitive. Which is how I found the idea of just doing a video game. And as I am a masochist, I decided to try to do an MMORPG.
  
It could be seen as not very sane to begin a project that you don’t really plan to finish. And I can agree with this opinion, but it is also a good thing as I don’t care about the speed at which the project is going on, I can take my time exploring each interesting subject I encounter one after the other. And having the “big project” as a guiding thread in order to always having something to work on.
   
Anyway, without an actual idea for the gameplay I just thought

> let’s do a MMORPG with final fantasy like turn based fights

And here begin the crazy adventure.

## What is your mindset as you begin your project ?


At that time, I was working as a java developer working on spring based middlewares frameworks in a bank.
But I wanted to do C++ on my free time, as I has lot of that those days (told ya I am a masochist), so I began watching all the cpp conferences from 2014 to 2017 (lot of videos) and I discovered how awesomely C++ evolved. Entering the modern era and being more attractive and interesting than ever. I decided to dive into it, special thanks to [Scott Meyers](https://web.archive.org/web/20201107223744/https://fr.wikipedia.org/wiki/Scott_Meyers) books ([effective modern C++](https://web.archive.org/web/20201107223744/https://www.amazon.fr/Effective-Modern-C-Scott-Meyers/dp/1491903996?SubscriptionId=AKIAILSHYYTFIVPWUY6Q&tag=duc-21&linkCode=xm2&camp=2025&creative=165953&creativeASIN=1491903996), [Effective C++](https://web.archive.org/web/20201107223744/https://www.amazon.fr/Effective-Specific-Improve-Programs-Designs/dp/0321334876?SubscriptionId=AKIAILSHYYTFIVPWUY6Q&tag=duc-21&linkCode=xm2&camp=2025&creative=165953&creativeASIN=0321334876)), I open a parenthesis to say that this is one of the best C++ content I read overall and I warmly recommend it to anyone wanting to learn more about the new features of C++ from 11 to 14.
And it basically made me change my job in order to get more experienced in the language and, hopefully, trying to become a C++ expert some days.


At this point, I wasn’t disappointed with my choice. The number of subjects covered by this project was enormous as where the number of decisions to take.

{{< notice question >}}
- What network library should I use?
- UDP/IP or TCP/IP protocol?
- What kind of serialization to use?
- What is the best way to do software development in the video game industry?
- What should be the server architecture? Scalability?
- What Database should I use, should I even used a Database?
- What Scripting language?
{{< /notice >}}

The goal of this blog is for me to explain the thought process I had, the reason I did the choices I did, and the reason I stepped back in the certain choices I made.
So we could say I am planning on doing a memento to keep track of my own reasoning while trying to give you the original source where I found the different information helping me making my choices.
But obviously not in the order I actually did those choices, it would be way too messy and hard to follow. So I will do it from what I think can be called a “logical” order.
Because as you can already see, there are many of them, and as every developer, we have our “default” choices when it comes to libraries and technologies to use. Even though it is, sometimes, not the wisest choice.


{{ < notice note > }}
My focus is on architecture and server design
{{ < /notice> }}

# The first decisions


My very first decision was to keep it simple concerning the graphics, I don’t have great interest in the client side code (at least concerning the graphics), I would prefer using a game engine but I also didn’t want to enter into a hard and long learning curve with a game engine that doesn’t interest me in the least (at least currently).
My focus is on architecture and server design which is why I decided to have my client in 2d. Another obvious reason is the following, the available free models in 3d are really limited while the 2d tiles are everywhere on the web just to enumerate the most famous sprite/tiles supplier websites :
 - https://opengameart.org/  
 - https://www.gamedeveloperstudio.com/  
 -  … and a lot of others, interesting to note that Unity is offering some 3d and 2d game assets. But clearly not enough for doing more than just a demo to play with the game engine.  

But even there, it is not that easy, I took the FF6 sprites sheet from opengameart. And I tried to naively make the map myself. It’s hard, very long and error-prone work. So I (very quickly) decided to use something to help me with the map building.


Firstly, the idea of using coco2d came to my mind. But the setup was slow and I had the feeling of entering into the “learning curve” that I didn’t want to enter with unity (at least not at this moment), the tool was way too powerful/overkill for what I planned to do with it.
And then, I remembered the amazing tools I used in my school days: Tiled. A very complete and powerful map editor developed by Thorbjørn Lindeijer aka Bjorn on Github which is heavily maintained and used.
It suddenly became very easy to create a map with very complex tilesets like the FF6 one. I just took a minimalist SFML project to display the map. And I was done (as I just wanted this in order to begin my game).



