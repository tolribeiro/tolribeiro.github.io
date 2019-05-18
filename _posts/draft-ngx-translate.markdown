---
title: "Speeding up content translation with Node script (ngx-translate helper)"
layout: post
tag: node
blog: true
comments: false
---

Let's be honest...nowadays, achieving internationalization has basically become a must. A web app that is translated into multiple languages has become
not only important, but kind of vital, for any business that already acts or aspires to reach global impact. 

In case where the project is in Angular (or any modern framework I would believe), you're covered. Without starting a (strikethrough)war conversation about wheter to use something 
like ngx-translate or the built in Angular i18n (btw, there is a good response to that question from Olivier Combe / @ocombe https://github.com/ocombe from the Angular team about it) 
let's just consider that I've had to maintain a project using the former.

After going back and forth in between comps, copying and pasting the strings on Google Translator and then mapping them to their respective keys, I decided to create 
a simple script to do it for me, which turned out to be almost 5 times faster than when I used to do the process manually!

//gif garotinha chorando 

Automatically generating the mapping

Considering a mapping structure where we have a `string.ts` file declaring the constants, and then a `en.json` and `es.json` files within some `i18n` 
directory specifying the respective expected texts in English and Spanish, our last job becomes the use of a piper within the template for it to work like magic.

Before that is where the script comes handy by creating the string constant and its translation for the three sets of these string files (one for the main string file, one for English and another one for Spanish). 
So with that, whenever I have to go over some comps to start writing the template, you can copy and paste the texts that will appear on the page inside a `input.txt` file, choose the language to translate it and run it.

Right now we do not support other languages, but as the app scales, I assume other languages are going to be added to the `i18n` folder, and the time it’d take to repeat this process, which already is long enough for two languages, would exponentially grow. Therefore, this can help us save tons of hours of tedious manual stuff and focus on implementation instead.

Link to the script repo: https://github.com/tolribeiro/nischt.

The idea for the future is to use something like Tesseract to extract the text from the comps and create the `input.txt` automatically.

As an example, this would be an `input.txt` for this screen:

