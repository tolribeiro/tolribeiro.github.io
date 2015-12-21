---
layout: post
title:  "Digital Modulation: using PSK as example on MATLAB."
description: "How to use MATLAB to explore and practice digital modulation."
date:   2014-10-30 21:53:05
categories: jekyll update
---
This semester I had some exposure to digital modulation and learned some techniques applied to the studies of Communications Systems, which we'll put into practice by using the powerful software MATLAB.

For this tutorial, I'll pick up the **PSK** (Phase-Shift Keying). It uses shifts in phase of a signal to represent data. However, if you want and feel comfortable, you can also try it using *ASK*, *FSK* or *QAM*, that along with PSK, form the group of main types of digital modulation widely used in a variety of modern systems, such as cellular networks and so on. 

First, let's suppose we have a message *m(t)*, which is a bit-stream signal, that we want to send through an analog channel. For this example, we consider the frequency of *m(t)* as *2 Hz*. Therefore, we have:

{% highlight matlab %}
f2 = 2;                       	% m(t) frequency
t = 0:.001:1;			% time definition
m = square(2*pi*f2*t);          % message 
subplot(3,1,2);
plot(t, m);                     % plotting m(t)
xlabel('Time');
ylabel('Amplitude');
title('Message Signal m(t)');
grid on;
{% endhighlight %}

After running this, you should see this image, which represents the message we wanna send: 

<div style="text-align:center" markdown="1">
<!-- ![Message Signal](http://tolribeiro.github.io/mywebsite/downloads/message.png "Message Signal m(t)") -->
<img src="./static/img/message.png"/>
</div>

Now we can write the definition for the carrier *x(t)*, a *sin()* function with frequency of *10 Hz* and amplitude *A* of *5*.

{% highlight matlab %}
A = 5;                        % amplitude
f1 = 10;                      % frequency
x = A.*sin(2*pi*f1*t);        % carrier function
subplot(3,1,1);
plot(t, x);                   % plotting x(t)
xlabel('Time');
ylabel('Amplitude');
title('Carrier x(t)');
grid on;
{% endhighlight%}

Now we can see the carrier *x(t)* we're gonna use to modulate our message *m(t)*:

<div style="text-align:center" markdown="1">
<!-- ![Carrier Signal](http://tolribeiro.github.io/mywebsite/downloads/carrier.png "Carrier x(t)") -->
<img src="./static/img/carrier.png"/>
</div>

Finally, we can plot the modulated (in phase) signal *u(t)* by just multiplying *m(t)* by *x(t)*. We're gonna call *u(t)* the modulated signal.

{% highlight matlab %}
v = x.*u;                      % Carrier multiplied by message
subplot(3,1,3);
plot(t, v);                    % Plotting u(t), modulated signal
xlabel('Time');
ylabel('Amplitude');
title('PSK Modulated Signal u(t)');
grid on;
{% endhighlight%}

Which we can see as:

<div style="text-align:center" markdown="1">
<!-- ![Modulated Signal](http://tolribeiro.github.io/mywebsite/downloads/modulated.png "PSK Modulated Signal u(t)") -->
<img src="./static/img/modulated.png"/>
</div>

Finally, our message is modulated in **PSK**, once the phase of the signal does not change while *m(t)* is equal to *1*, being reversed (changing by 180 degrees) when it goes to *0*.
