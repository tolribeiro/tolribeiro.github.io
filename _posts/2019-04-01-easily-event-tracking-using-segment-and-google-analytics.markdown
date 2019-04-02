---
title: "Easy event tracking using Segment and Google Analytics"
layout: post
tag: segment
blog: true
comments: false
---

> Truth is always to be found in simplicity, and not in the multiplicity and confusion of things
> **Isaac Newton**

This quote from Newton has recently become my motto. Along with the divide-and-conquer approach to problem solving, these two ideas together become a powerful concept to remind yourself of whenever a challenge comes up.

Not that integrating some analytics into a project should be something very complicated to accomplish, but depending on the documentation of the service you want to use and the task at hand, things can get a bit tricky.

### It should not be painful...

If you've had experience integrating third-party APIs into any project, you've probably had to deal with some unpolished docs out there that instead of clarifying stuff, leave you even more confused than when you started reading them.

Here is an important point on that: when a company's target market involves developers, this is something to keep an eye on. John Collison from Stripe can back me up on that when he affirms that their great API and documentation were important factors for <a href="https://growthhackers.com/growth-studies/how-stripe-marketed-to-developers-so-effectively" target="_blank">Stripe's success</a>.

And that's where Segment comes into play.

### KISS principle at its core

On that matter, Segment definitely got it right. Learning to integrate event tracking into your project becomes very simple, straight to the point. Let me show you an example.

Let's suppose you have a search bar on your website and you just need to track the words people are searching for. Check this out (Javascript):

```
analytics.track ("Searched", {
  searched_word: "medicine",
});
```

That's all you'd need: the **action** you want to track, and the **property** to capture the user's searched word.

Nevertheless, even though you can send all sorts of custom properties to Segment (and check them on the debugger for testing purposes), it apparently does not keep these values ​​stored in there. For that, you have to connect your project to a destination (such as GA) you want to send these events to so they can be stored, exported and analyzed there instead.

### Checking the searched words on Google Analytics

Once Segment is receiving your events and they match the payload you expect on the debugger, you need to create the link to GA. Here are the steps:

1. **Create Custom Dimensions on GA:** this needs to be done so Segment can link the custom property name you chose, to these "dimensions" (or variable names);
 <img width = "599" alt = "Screen Shot 2019-04-01 at 10 00 57 AM" src="https://user-images.githubusercontent.com/6345197/55353750-b70f5980-5489-11e9-8cd2-13c82301d2b9.png">
2. **Map property to dimesion index on Segment:** on the GA settings on Segment (Destinations), link them using its index:
<img width = "577" alt = "Screen Shot 2019-04-01 at 10 00 46 AM" src = "https://user-images.githubusercontent.com/6345197/55353814-d4dcbe80-5489-11e9-9526-17a9dab692f6.png">
3. **Select the Dimension for the event action:** Once you get to the Events page and select the action ("Searched" on our example), you can select the Custom Dimension and you'll be able to see the list of searched words.
<img width = "340" alt = "Screen Shot 2019-04-01 at 1 23 39 PM" src = "https://user-images.githubusercontent.com/6345197/55353844-e1f9ad80-5489-11e9-801f-e613dc0cf321.png">

That way, you can leverage the amazingly powerful features of GA and Segment's event tracking library all at once.

Next time you need to track events on your website or app and you already use Google Analytics, this is definitely a combo you should try out since I do not think it can get any simpler than that!