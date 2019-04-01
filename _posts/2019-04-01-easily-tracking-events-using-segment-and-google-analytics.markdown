---
title: "Easily tracking events using Segment and Google Analytics"
layout: post
tag: segment
blog: true
comments: false
---

### Easily tracking events using Segment and Google Analytics

> Truth is always to be found in simplicity, and not in the multiplicity and confusion of things
> Isaac Newton

This quote from Newton has recently become my motto. Along with the divide-and-conquer approach to problem solving, these two ideas together become a powerful concept to remind yourself of whenever a challenge comes up.

Not that integrating some analytics into a project should be very complicated to accomplish, but depending on the documentation of the service you want to use and the task at hand, things can get tricky bit.

### It should not be painful ...

If you've had experience integrating third-party APIs into any project, you've probably had to deal with some unpolished docs out there instead of clarifying stuff, leave you even more confused than when you started reading them.

Here is an important point on that: when a company's target market involves developers, this is something to keep an eye on. John Collison from Stripe can back me up on that when I affirm that their great API and documentation were important factors for [Stripe's success] (https://growthhackers.com/growth-studies/how-stripe-marketed-to-developers- so-effectively)).

And that's where Segment comes into play.

### KISS principle at its core

On that matter, Segment definitely got it right. Learning to integrate event tracking into your project becomes very simple, straight to the point. Let me show you an example.

Let's suppose you have a search bar on your website and you just need to track the words people are searching for. Check this out (Javascript):

(I.e.
analytics.track ("Searched", {
  searched_word: "medicine",
});
(I.e.
That's all you'd need: the ** action ** you want to track, and the ** property ** to capture the user's searched word.

Nevertheless, even though you can send all sorts of custom properties to Segment (and check them on the debugger for testing purposes), it apparently does not keep these values ​​stored in there.
 
For that, you have to connect your project to a destination (such as GA) you want to send these events to so they can be stored, exported and analyzed there instead.

### Checking the searched words on Google Analytics

Once Segment is receiving your events and they match the payload you expect on the debugger, you need to create the link to GA. Here are the steps:

 - ** Create Custom Dimensions on GA: ** this needs to be done so Segment can link the custom property name you chose, to these "dimensions" (or variable names);
 <img width = "599" alt = "Screen Shot 2019-04-01 at 10 00 57 AM" src = "https://user-images.githubusercontent.com/6345197/55349829-46177400-5480-11e9-986d- de6b098df3e4.png ">
 - ** Map property to size index on Segment: ** on the GA settings on Segment (Destinations), link them using its index:
<img width = "577" alt = "Screen Shot 2019-04-01 at 10 00 46 AM" src = "https://user-images.githubusercontent.com/6345197/55350091-e2da1180-5480-11e9-8628- fb7011e35138.png ">
 - ** Select the Dimension for the event action: ** Once you get to the Events page and select the action ("Searched" on our example), you can select the Custom Dimension and you'll be able to see the list of searched words.
<img width = "340" alt = "Screen Shot 2019-04-01 at 1 23 39 PM" src = "https://user-images.githubusercontent.com/6345197/55350316-672c9480-5481-11e9-847a- 13d505e92833.png ">

That way, you can leverage the amazingly powerful features of GA and Segment's tracking event library all at once.

Next time you need to track events on your website or app and you already use Google Analytics, this is definitely a combo you should try out since I do not think it can get any simpler than that!