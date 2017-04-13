---
title: 'Random Sentence Generator - Javascript Tutorial'
date: 2013-11-02T19:06:22+00:00
author: Phillip Richter
layout: post
permalink: /javascript-for-beginners-random-sentence-generator/
categories: General
redirect_from: "/wordpress/javascript-for-beginners-random-sentence-generator/"
---
Sometimes it is usefull to have  an area on your website, where there are a few linked sentences, which are randomly choosen from a stock of sentences. Typical examples of use could be a glossary or advertising slogans. For this purpose I created a small javascript code-snippet for a random sentence generator, with which you can realize this easily.
  
The first thing you need to do is to create an array. To make it easy in the beginning, we will just assign plain text values in the array, without linking them or adding any further HTML-code. so let us start.

<!--more-->

## An array for our random sentence generator

<pre>var saetze = new Array();
saetze[0] = 'Lorem ipsum';
saetze[1] = 'At vero';
saetze[2] = 'sed diam.';
saetze[3] = 'Consetetur sadipscing.';
saetze[4] = 'Dolores et ea rebum.';
saetze[5] = 'sed at vero eos et accusam.';</pre>

This is an example of an array of six random sentences. Between the apostrophes you can enter your text, without any limitations in content or the number of values. Later on we will include HTML-tags into our sentences. But let us first code the heart of this little javascript widget: the loop of the random sentence generator:

## The for-loop is the heart of it

<pre>for (x=0; x&lt;2; x++){
	y = Math.floor(Math.random()*saetze.length);
	var div = document.getElementById('box3');

    div.innerHTML= div.innerHTML + saetze[y];
    saetze.splice(y, 1);
}</pre>

Here is how it is working: The for-loop is choosing, how many random sentences are shown at a time. In this example we have got two sentences. so the loop iterates two times. In the loops body we are generating a random number and multiplicating this number with the amount of variables we have in the array. With this little magic and the statement to create an integer value with &#8218;Math.floor&#8216;, we are getting a value for the y, which is representing one of our array-values. In the next step we are saving the HTML elements&#8216; ID, where we want to let our random sentences appear on our website, in a variable. In this example we choose the element with the ID &#8218;box3&#8216;. Finally we just replace the content of this element with our content we have got from the randomly chosen sentence. To avoid getting repetitions, we just need to delete the randomly chosen value of our array. And that is already it!

## Adding some HTML

Let us now include some fancy HTML functionality to our random sentence generator. This is not complicated at all. The innerHTML functionality of javascript allows us, to include HTML-tags into our quotes. We can, for example, easily link our sentences to other destinations. Here is some code to make things clearer:

<pre>saetze[0] = '<a href="whttp://www.bestinnotions.de">Lorem ipsum</a>';
saetze[1] = '<a href="whttp://www.bestinnotions.de">At vero eos</a>';
saetze[2] = '<a href="whttp://www.bestinnotions.de">sed diam nonumy eirmod tempor.</a>';
saetze[3] = '<a href="whttp://www.bestinnotions.de">Consetetur sadipscing elitr.</a>';
saetze[4] = '<a href="whttp://www.bestinnotions.de">Dolores et ea rebum.</a>';
saetze[5] = '<a href="whttp://www.bestinnotions.de">sed at vero eos et accusam et.</a>';</pre>

Here I just included the usual a-tag into my array-values. If you want to style every random sentence separatly with CSS you can as well add id&#8217;s and classes this way. To include HTML for all sentences, you do not need to change every single varibale, but may add the HTML to the loop. Here is the code:

<pre>for (x=0; x&lt;3; x++){
	y = Math.floor(Math.random()*saetze.length);
	var div = document.getElementById('box3');

    div.innerHTML = div.innerHTML + saetze[y] + '<br />';
    saetze.splice(y, 1);
}</pre>

Here I just added the break-tag to the loop. If you want, you can add any further HTML-code to the array-values and complete the code in the loop. If you want to give the link-tag a description, the same for every sentence, then you can do the following:

<pre>div.innerHTML = div.innerHTML + '&lt;a class="saetze" title="Klick mich" ';</pre>

It is impottant to add a white space after 'Klick mich', that concatination properly workds. In the values of the array you can now add the different link-destinations like this:

<pre>saetze[1] = 'href="http://www.bestinnovations.de/test">Lorem ipsum&lt;/a>';</pre>

As you can see, the values of the array and the innerHTML just got concatinated here. This gives you millions of possibilities, so this javascript random sentence generator is very flexible and can easily adapt to your needs.
  
I hope you enjoyed this little javascript tutorial. For a more fundamental introduction for javascript i can advise you the tut's from the <a title="codeacademy" href="http://www.codecademy.com/tracks/javascript" target="_blank">codeacademy</a>. We are looking forward for your comments.

Your web.studio Richter
