---
date: "2019-05-20"
title: "conference report : ACCU2019"
tags:
  - "conference"
  
draft: true
---

# Conference Report: ACCU 2019

I had the pleasure to attend to the [ACCU2019 in Bristol](https://web.archive.org/web/20190505052640/https://conference.accu.org/) which was my first cpp centred conference (the first of a long series I hope :p) and it was amazing in a different aspect.


It is a 4 days conference that occurs every year between March and April in the Marriott hotel in Bristol.


Amazing people, very inclusive and easy to talk to everyone!

Before starting with the report, I have to say that Bristol is a surprisingly beautiful city (at least for me, I was convinced it was going to a quite plain town) with a big shopping mall.

At the beginning I was scared that going alone to a conference where people already more or less know each other (and it is actually the case as most of the people regularly go to such conferences) I wouldn’t find a place into those already formed group. And here came the [PacMan rule](https://web.archive.org/web/20190505052640/https://www.ericholscher.com/blog/2017/aug/2/pacman-rule-conferences/) (Always let a room left for someone to join your circle when having a discussion, if someone join, give this person some context and continue), it may not be the only reason, but it certainly helped. I could very easily talk to anyone during the conference.

## The talks that I preferred

This is my personal opinion and doesn’t mean that the other talks weren’t good. I just need to narrow the number of talks I am going to be talking about in order to not have a 1000 thousand line blog 🙂
I remind you that all the talks are available on [YouTube](https://web.archive.org/web/20190505052640/https://www.youtube.com/channel/UCJhay24LTpO1s4bIZxuIqKw/featured).

### [Making exceptions more affordable and usable](https://web.archive.org/web/20190505052640/https://conference.accu.org/2019/sessions.html#XDefragmentingCMakingexceptionsmoreaffordableandusable) keynote by [Herb Sutter](https://web.archive.org/web/20190505052640/https://conference.accu.org/2019/presenters.html#XHerbSutter)

Explaining about potential upcoming C++ feature about making an exception without overhead, which would make everyone able to use it (as a lot of people in certain fields remove exception handling in order to not suffer the unnecessary overhead) and open the STL usage to anyone (as STL use exceptions).

{{ < youtube os7cqJ5qlzo > }}


### [More GDB wizardry and 8 other debugging tools](https://conference.accu.org/2019/sessions.html#XMoreGDBwizardryand8otheressentialLinuxapplicationdebuggingtools) by [Greg Law](https://conference.accu.org/2019/presenters.html#XGregLaw)

I may be ashamed to say so but, I didn’t know GDB at all actually. Only the basics of it and the help of IDE made it even worse as it was easier to add breakpoints instead of thinking how to do things in a smarter way.
In my current job, the toolchain we have to make it very hard to link our IDE with gdb (remote desktop combined with the internal build system and so on), so we have to use it in terminal mode. And this talk changed my vision of gdb into “it’s a pain to use it” to “it’s an out of the box over powerful tool”. Who knew about the TUI? I can at least say not many people attending this conference and I never saw its usage in actual gdb tutorials (the gdb official documentation being very messy and not attractive).
This talk also speaks about the other debugging tools (Valgrind, Callgrind, strace, etc…) but the talk is mainly centred on gdb.

{{ < youtube Yq6g_kvyvPU > }}


{{ < notice note > }}
Key things to remember on GDB from this talk :

- GDB TUI (textual user interface): which helps a lot while using gdb in terminal mode
- dprintf (dynamic printf): who recompiled its code countless times to add a log? I confess.
- pretty-printer: who did call vector.at(int) to check the content of a vector (either via printf of in gdb)? I confess again :p

{{ < /notice > }}

### [What Do We Mean When We Say Nothing At All?](https://conference.accu.org/2019/sessions.html#XWhatDoWeMeanWhenWeSayNothingAtAll) by [Kate Gregory](https://conference.accu.org/2019/presenters.html#XKateGregory)

Very interesting talk, overall intuitive (for example, if constness is always respected, when no const present that means the method/parameter is mutated in the scope) but this talk go much deeper and talks about other aspect like, keeping old for loop in order to attract attention on the fact that the logic into this specific for loop is more complex and require special attention.
This is, in my personal opinion, a utopian view (as she explains herself in the Q&A) as it works only if you are extremely consistent in your way of developing, always following the same patterns. And if you are a team member, this means those patterns have to be accepted and respected by each member of the team. Which is not as easy as it would seem from an external point of view (just do a confluence page with the rules and everyone follow them… Already tried, it doesn’t work that well).
But the talk is worth watching and could give good easy to follow guidelines to a development team.

{{ < youtube -Hb-9TUyjoo > }}

### [Hello World from Scratch](https://conference.accu.org/2019/sessions.html#XHelloWorldfromScratch) by [Peter Bindels](https://conference.accu.org/2019/presenters.html#XPeterBindels) and [Simon Brand](https://conference.accu.org/2019/presenters.html#XSimonBrand)

The title could be misleading, this talk talks about a single line code in c++, what happens from the code to the compiler, to the binary passing by the generated assembly.
I basically had no real knowledge about how a compiler actually worked when entering the conference room and I found this talk to be a very good introduction of how a compiler actually works as it explains each layer on by one (dodging the syntax interpretation part.. as it wasn’t a 10h talks it’s understandable).

{{ < youtube MZo7k_IOCe8 > }}

It would deserve a second part in order to add details and go deeper in how the compiler works, if one arises I will be the first one to watch it.

### [10 Techniques to Understand Code You Don’t Know](https://conference.accu.org/2019/sessions.html#X10TechniquestoUnderstandCodeYouDontKnow) by [Jonathan Boccara](https://web.archive.org/web/20190505052640/https://conference.accu.org/2019/presenters.html#XJonathanBoccara)

just one advice, do not stop watching after the 10 first minutes (as the first advice are quite common sense), some interesting techniques based on word counting and others are following. Some tools developed by [himself also exist to try those techniques](https://www.fluentcpp.com/word-count/).
Those are quite interesting ways of approaching new code that I will try at work more often (currently working on a big legacy based project).


{{ < youtube tOOK-VsWU-I > }}


### All talks were good

Some funnier than others

I can only advice to see Patricia Aas talk about exploit (very funny and explain the basis that only a few has about software exploit). This will certainly not be useful in your everyday work, but it will remind you that you must be careful about what you do.

**Type safety topic is hot those days**
Strong type is more and more a hot topic these days, it is not surprising to see some in ACCU. If you never heard about it, those talks are very interesting to watch as you will certainly learn what strong typing is for. The usual example of the Mars Climate Orbiter has obviously been used :p

Safe and Sane C++ Types by Peter Sommerlad
The advice about security keynote by M Angela Sasse was very interesting and talks to most of the people working in IT, which makes it quite funny.

and many others...

I am planning on catching up with the other talks on youtube and you may want to give it a shot.


Amazing goodies :p