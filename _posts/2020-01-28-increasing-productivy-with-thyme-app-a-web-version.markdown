---
title: "Increasing productivity with Thyme app: a web version"
layout: post
tag: time tracking thyme
blog: true
comments: false
---

------------------------------------

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/73285386-91430600-41bb-11ea-8016-cde93451d400.jpg" width="699" class="img-responsive center-block" />
</div>

# Looking for a way to increase your productivity?

Have you ever had those moments where you're looking for an application to fulfill some specific need? I bet you have.

That's how I found myself last year: looking for ways to increase my level of concentration and productivity while focusing on a single task.

Among the several ways you can accomplish that, for me, the main thing I was looking for was to simply track *time spent working deeply on something* (yes, Carl Newports' <a href="https://www.calnewport.com/books/deep-work/" target="_blank">Deep Work</a> book did have an influence on that).

Although I did find several cool options out there (<a href="https://toggl.com/">Toggl</a>, <a href="https://tickspot.com/" target="_blank">Tickspot</a>, etc),  everything I tried didn't feel right.

Some of the other solutions I found were either full of features I didn't need, or I'd have to pay to use it or sign up to at least see it functioning. 

Until I found <a href="https://joaomoreno.github.io/thyme/" target="_blank">Thyme</a>. With no expectations (since it was free and open source), I downloaded it, tried it out for a couple of days and...loved it. The app was simple and straight to the point. 

As I was using it, I was noticing how much more focused and productive I'd become while working on something and I am very sure the app has me helped to achieve that. I had finally found exactly what I was looking for.

# My workflow with Thyme

It seems very obvious, but Thyme seems to get the UX involved in the process of tracking your time, more naturally by dividing it into *three* actions: *start*, *stop* and *continue*. 

That idea contrasts with a lot of what you'll see out there with the "Start" and "Stop" button titles only. 
 
Even Google's timer (Apple's too I should say) shows the word "Start" when you stop the timer after awhile, which feels a bit weird to me since I don't feel like I'm starting. I'm continuing or resuming (UI/UX folks out there, what do you think?) a task. 

Back to Thyme, there is also a little feature that comes in handy, which is the export option.

Overall, the idea of a timer is straightforward, but the solutions I had found prior to Thyme all seemed overly engineered which distracted me from the real objective: helping me track how long did it take to finish a task.

# Con: Thyme is Mac OS only

Hopefully I've convinced you that that little app is awesome by now, but the con is that Thyme is currently only written for Mac OS (until now I guess). 

As I have been using Windows a lot for the past months, I just started to feel the void. The daily use of the app stuck like a habit.

It had become part of my daily activities and I was missing it a lot. It had definitely become part of my daily routine: sit down to concentrate, 
start Thyme. Then I had an idea...

# Thyme Web version

I decided to create a web version of that lovely app, trying to mimic the experience you get on the Mac OS native app as much as possible.

As this is an initial version, and as one of the responsible for maintaining the OS X app (you can check the repository <a href="https://github.com/joaomoreno/thyme" target="blank_">here</a>), I've obviously also decided to make it open source. 

The project is written in Angular and uses Web Workers to keep the timer being updated even if you switch tabs or minimize the browser. 

The beautiful UI you see was created in partnership with <a href="https://dribbble.com/jandui" target="blank_">Jandui</a> (thanks my friend!) which I've successfully been able to convince to start navigating the open source world as well, haha. 

This very first version is available here on <a href="https://thymeweb.netlify.com/">https://thymeweb.netlify.com/</a>

# Current Features

 - Basic timer (just like the original Thyme);
 - Option to export list of worked tasks as `.txt`;
 - Tagging tasks when finished;
 - Local storage (tasks are kept even if tab/window closes);

# Future Additions

- **Synching capability**: since I have noticed that as I have the app installed in multiple Mac machines, and Thyme for Mac stores it locally only, I end up not knowing anything about my tasks from one machine once I switch to another;
- **Fully developed mobile UI**: for now only the Desktop app looks good, but we've got some work to finish the mobile version of it;

Interested? please star the repo (<a href="https://github.com/tolribeiro/thyme-web" target="blank_">https://github.com/tolribeiro/thyme-web</a>) and help us spread the word about Thyme. You are more than welcome helping us out to build a better version of it :)

And I hope Thyme becomes as useful and helpful to you as it has been to me (I've used the web version to track the time I spent writing this post as well!)
