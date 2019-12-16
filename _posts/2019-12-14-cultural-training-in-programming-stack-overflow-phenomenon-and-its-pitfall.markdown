---
title: "Cultural training in programming: the pitfall of the Stack Overflow phenomenon"
layout: post
tag: programming
blog: true
comments: false
---

------------------------------------

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/70920688-9ae82400-1fe8-11ea-9ecb-f927c4232d71.png" width="699" class="img-responsive center-block" />
</div>

# A little story on cultural training: grandma's ham

A couple of years ago I once read a fictional story on a book that resonated so much with me that I could never forget it. 

It talked about a family event where a husband and his wife were in their kitchen and he was sitting at the table reading the newspaper while she prepared a ham for dinner. 

At some point, he observed that she was cutting off about one inch from either end of the ham and then he asked: "Why are you doing that? that's such a waste of good ham!" to which she promptly responded: "that’s the way my mom has always prepared it". When he asked *why* her mom used to do that, the wife simply didn't know the answer.

Now in the search for it, she called her mom to ask: "Mom, why do you cut the ends of the ham off?". "Well, because that's the way my mom used to do it".

Though the wife's grandma had passed away, her grandpa was still alive. Still without the answer, she then called him to ask: "Grandpa, would you know why my grandma used to cut the ends off of the ham?" He was silent for a moment and then replied, “Well, she used to do that so the ham could fit in the baking pan.”

This story illustrates what is often called **cultural training** which is when one generation (or employee) teaches or passes down a process or knowledge to another. 

# Stack Overflow: cultural training at scale

If you're a software engineer or have interacted with them for long enough, you've probably heard of Stack Overflow at least once in your life.

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/70921763-8dcc3480-1fea-11ea-951a-0c1abed6ad43.jpeg" width="600" class="img-responsive center-block" />
<div style="text-align:center" markdown="1">
<span style="color:#aaa;">Jeff and Joel giving a speech one year after the website's launch (2009)</span>
</div>
</div>


Created in 2008 by <a href="https://en.wikipedia.org/wiki/Jeff_Atwood" target="_blank">Jeff Atwood</a> and <a href="https://en.wikipedia.org/wiki/Joel_Spolsky" target="_blank">Joel Spolsky</a> (the same guy that created Trello, which I wrote about <a href="https://toribeiro.com/taking-your-trello-board-to-the-next-level-essential-plugins-to-boost-its-power/" target="_blank">on my previous post</a>), it's a question and answer website for programmers to post and answer questions related to programming languages, problems and general issues.

As of January 2019, the platform had reached over *10 million* registered users and it exceeded *16 million questions* in mid 2018.

Given these absurd numbers, you can quickly realize the impact it's had in the life of millions of programmers around the globe, becoming one of the most used tools used for helping to solve tough day-to-day questions and problems that are very common in the life of a software engineer.

But as the popular Peter Parker proverb states, *with great power comes great responsibility*. Now 11 years after its launch, it seems like the responsibility aspect of it is starting to catch up. The evidence is <a href="https://www.zdnet.com/article/the-most-copied-stackoverflow-java-code-snippet-contains-a-bug/" target="_blank">this article</a> I stumbled upon recently that mentioned that <a href="https://programming.guide/worlds-most-copied-so-snippet.html" target="_blank">the most copied Stack Overflow snippet of all time is flawed</a>.

The answer to the the question *"how do you print a byte count in a human readable format"* or *"how do you format something like 123,456,789 bytes as '123.5 MB'?"* had been copied and embedded in more than 6,000 GitHub Java projects (!)...and *it contained a bug*. The admission came 9 years later from the author of the snippet itself, <a href="https://aioo.be/" target="_blank">Andreas Lundblad</a>, a Java developer at Palantir.

That comes to show something I consider a recent phenomena in our profession: it seems that *a lot of us have become bound to simply replicate code or patterns without giving it a second thought or analysis*, imitating exactly the same behavior of the fictional wife preparing the ham from the story above. In order to break that cycle, I'd argue that a simple way would be to willingly force ourselves to start using the word *why* more often.

# Escaping the blind replication trap: always ask why

I've always been a curious kid and soon have learned that in order to undersand something the best way, I'd have to ask myself *why* things are the way they are. I confess, though, that this is not always a self-conscious thought process that I go through for every thing I do in life, but it certainly is reinforced whenever I sit down to write code or design a solution to a problem. 

One common thing I've seen a lot outside of the Stack Overflow example, is in large codebases where things were written a certain way and new developers tend to believe that since something is written or architected like that, then things should simply be replicated without questioning. 

During my own journey, I've constantly tried to train myself to stop whenever I'm about to replicate a pattern, a snippet or a certain way of doing things, and ask: "why am I doing it that way?". That has proven to help me build my confidence in the very early stages of my career and until today has kept me challenging myself to see things on a different light.