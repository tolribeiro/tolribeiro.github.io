---
title: "Taking your Trello board to the next level: essential plugins to boost its power"
layout: post
tag: trello
blog: true
comments: false
---

------------------------------------

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/69908242-2b98f000-13ab-11ea-9c1e-20542d41725e.png" width="800" class="img-responsive center-block" />
</div>

## Why and when to use a process like Kanban?

One of the most important parts of the process involving the design and analysis of systems is the proper choice of the methodology to be used throughout the implementation phase.

In the case of systems modest in size, operating with relatively small teams, aiming to release software early and often without having to follow the constraints of a more rigid approach, a list of ideal characteristics that fits these requirements would probably look something like this:

* Little to none distinction amongst roles;

* High flexibility to change;

* Estimation based on cycle time; 

* Variable prioritization;

Sounds familiar? well, yes. We are describing *Kanban*. 

In the very early phases of <a href="https://jampapp.com" target="_blank">Jamp</a>, we naturally discovered that this methodology worked great for us and have decided to keep it until today. 

# Are there good Kanban tools out there?

As you might've guessed, with a very quick search you can find several long lists with tools that can be leveraged to implement Kanban into your project. 

However, for one reason or the other, Trello seems to be the go-to tool when we think about it. 

Maybe because of its simplicitity, maybe because it's free and with out-of-the-box features ready to use, or simply because it seems to be the best on the market (in my personal experience, I always seemed to go back to it after trying out others).

# Pro Trello & Parent/Child Dependency (PCD)

Although Trello holds its reputation through the advantages mentioned above, if you needed to rely on it for collecting metrics or even trivial tracking, it usually doesn't get you too far. 

The only way I found to keep using it and still extract valuable data from it, was by using these two amazing Chrome extensions: <a href="https://chrome.google.com/webstore/detail/pro-for-trello-free-trell/hcjkfaengbcfeckhjgjdldmhjpoglecc?hl=fr--------" target="_blank">Pro4Trello</a> and <a href="https://chrome.google.com/webstore/detail/parentchild-management-fo/flnpbgmiploomjgagfbcjlikpiehclld?hl=en" target="_blank">PCD</a> . 

# What are the advantages of using these extensions?

### Categorization

Since we have a couple of different systems and applications to keep track of, we've decided to use the ProTrello's categories feature per card and we divide them between iOS, Android, Website and others. 

So the user would start by typing the name of the category, then writing the description of the card after the pipe:

```
Category1 | This card is to describe a certain feature...
```

### Tagging

Each card that gets added to the board needs to specify its type through a tag. In our case, we have US (for User Stories) and DE (for defects). 

```
Category1 | This card is to describe a certain feature [US]
```

### Identification:

Since we need to keep track of which the changes to the codebase are related to each cards, this feature allows the developers to have an auto generated ID for each card created that can be used for branching or commit messages.

### Prioritization

Another key thing to differentiate cards is the ability to mark some as more important than others. For this, the plugin allows you to simply specifiy the level of priority of a card by using `!`, `!!`, or `!!!`.

### Estimation:

The person creating the card can also add the estimation for the time that is going to be spent on the task by adding a `{}` with the time inside the curly braces.

### Dependency

Finally, as sometimes needed, a task is dependent on the other and for that  we use PCD. Every time you open a card, this plugin shows a dropdown list that you can relate the current open card to its dependent.


## Real life example: defect on iOS app

Given that we need a card to track a defect (*tag:*`[DE]`) from the Jamp's iOS app (*category:* `iOS`) where the text gets truncated for words of more than 10 characters and it's a critical issue (*Prioritization:* `!!!`). 

The developer estimated that it'd take 1 hour to fix it. Here is how the card would be created for Pro4Trello:

```
iOS | {1h} !!! Fix truncated text for words of more than 10 characters [DE]
```

The plugin would then process these formatting from the card and display it like this:

<div style="text-align:center" markdown="1">
<img src="https://user-images.githubusercontent.com/6345197/69908127-00ad9c80-13a9-11ea-9aad-0bd2aa8dddf6.png" width="242" class="img-responsive center-block" />
</div>

Notice that it created its own id `#1`, which is used for commits and branches.

Now the most incredible part is that Pro4Trello organizes all the data for you on a tab below it, where you can simply on the filter (*category*, *tags* etc) and have the board display it for you:

<div style="text-align:center" markdown="2">
    <img width="615" alt="Screen Shot 2019-11-30 at 7 42 32 PM" src="https://user-images.githubusercontent.com/6345197/69908152-92b5a500-13a9-11ea-9380-d51e8e9a6c85.png" class="img-responsive center-block">
</div>

Therefore, by the end of each cycle (be it a week or two), you can archive the lists and they can be easily searched by dates from the default Trello search option. 

That way, we've been able to fully function as a small concise team by leveraging these tools which reduces eliminates the need to spend on more powerful ones since we'd only make us of some of its features.