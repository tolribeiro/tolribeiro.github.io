---
layout: post
title:  "My very fist iOS App: controlling work hours"
description: "A very simple app to help couting hours at work"
date:   2015-09-27 20:13:05
categories: ios app hours work control
---
In the month of May this year, I decided to dive into the world of mobile development. For that reason,  I accepted the challenge of joining a company specialized in a field where I would learn, practice daily, and immerse myself in the culture of developing applications that run in smartphones--specifically iPhones. 

Consequently, in the initial days of my internship, I was told that I should fill out a spreadsheet (on paper, it couldn't be digital) stating: the arrival time, if I had stopped to eat during the day, and my time of departure. 

Even though I had heard there was a spreadsheet set up that could do the job, I saw in that an opportunity to develop my skills in iOS--it was then that I began to create an app to do all the math for me. As a result, my only  task would be to log my work hours on the sheet at the end of the workday. 

<div style="text-align:center" markdown="1">
<!--![Message Signal](http://tolribeiro.github.io/mywebsite/downloads/minhasHorasNoData.jpg "First screen, to fill out with the times.")-->
<img src="./static/img/myHoursNoData.png" width="360" height="640" class="img-responsive center-block" />
</div>
<br />
In the empty forms, I manually enter the times (24-hour style in Brazil) during the day and press calculate to see how many hours I have worked until the break, the duration of my break, the hours I have worked after my break, and the total, as you can see below: 
<br />

<div style="text-align:center" markdown="1">
<img src="./static/img/myHoursData.png" width="360" height="640" class="img-responsive center-block"/>
<!--![Message Signal](http://tolribeiro.github.io/mywebsite/downloads/minhasHorasData.jpg "App showing the elapsed time calculated.")-->
</div>
<br />
As I kept researching about how to calculate elapsed time, I learned more about `NSDate` and `NSTimeInterval`, which I believe is a more appropriate way to implement such apps. Therefore, at the time, I designed the algorithm "by hand", by getting the interval between the integers and returning the elapsed time. 

After a couple of months, I considered a lot of other features that I could implement to make my app much more robust, such as: storing the data, enabling the user to use the current time from the phone to mark the time, and so on. 

Despite not yet implementing these features in my app, the experience of starting something on my own for iOS as a first application, even with such a simple function, was very encouraging and continues to keep me excited about the world of mobile development.
