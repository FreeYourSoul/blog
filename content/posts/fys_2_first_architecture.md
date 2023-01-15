---
date: "2019-04-29"
title: "FyS : frst architecture"
tags:
  - "freeyoursoul story"
  
draft: true
---

# The First architecture part-1

## Data-Oriented Design

We directly begin with one of the topics I took most of my time working on. For the people not familiar with Data Oriented Design (DoD), I will try explaining it in this post. But I will also give several links to content that are, I think, needed in order to grasp the importance and power of DoD in C++.


## The Goal of DOD in resume

Year after year, the processors are getting more and more powerful with many improvements.
But what is slowing down your application in this modern CPU time?
As of today, what is taking the most in modern application, it is data/memory access. Fetching data in a database is known as being a very time-consuming thing for instance. But it is also true at a lower level, in the level of the CPU cache and the ram that is.

As a good introduction, we could give the answer to the eternal question beginner in C++ ask: “Should I use vector or list ?” and the academic answer being “If recurring insertion/deletion of items are going to happen, use list. Otherwise, use vector”. Well, it is actually well known that you should use vector in 98% of the cases.
The following presentation by Bjarne Stroustrup about this subject, explain why.

{{< youtube YQs6IC-vgmo >}}


Ok so, from this talk we can say that memory alignment of our data structures are important.

Actually, taking care of the layout of the data structure you are doing in C++ is one of the secrets of good c++ development.
If you keep that in mind while coding and doing your software architectures, you certainly are in a good way for an efficient program ( at least I guarantee better than if you were not taking care of it :p ).

## Best sources on DoD

This article has for purpose to introduce you to the concept itself, but I don’t need to spam you with a thousand lines of explanations or a thousand different links on the subject as some people already did it for me (thanks to them all 🙂 ).
An amazing git repo that is only containing link about data oriented design
https://github.com/dbartolini/data-oriented-design

I am still going to give you the links that I found the most useful and introduce me to the DOD world, but do not hesitate to check all the others too.

* I am a fan of Scott Meyers books, and presentation so the first one will be his 🙂
To play this video, view this post from your live site.

https://vimeo.com/97337258


Despite not being a C++ lover, Jonathan Blow (developer of the indie video game Braid) is a good teacher and explain technical concepts very well. He is one of the first sources I had in order to understand how to take the data structure into consideration.
He is developing his own language which is game development oriented and try to hide complex DoD mechanisms to the user by combining easy to read “Object Oriented” coding style with “Data-Oriented Design” efficiency (I put quotes because its important to understand that one doesn’t exclude the other at all, this language makes it easier to do so).

For example, in his language, a vector<Struct> Struct being an object containing, for example, a string, an int and a double, will internally result in the creation of 3 different vectors (one of each type) in order to keep cache coherency. Well, to sum up, he has multiple videos on the subject that are very good in order to understand the concepts.
To play this video, view this post from your live site.

{{< youtube ZHqFrNyLlpA >}}


https://bitsquid.blogspot.com/2015/06/allocation-adventures-1-datacomponent.html

The Architecture I ended up will be explained in more detail in the part-2 of this article suite.

