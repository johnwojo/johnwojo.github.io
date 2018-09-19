---
layout: post
title:      "New library, who dis? An intro to jQuery."
date:       2018-09-19 21:25:09 +0000
permalink:  new_library_who_dis_an_intro_to_jquery
---


jQuery is a light-weight, cross-broswer, open-source JavaScript library that bestoys upon a developer a number of  powerful abilities. It is one of the most popular and easy to use JavaScript libraries and has been an exciting addition to my programming toolkit. 

![Suit up](https://media.giphy.com/media/lXo8uSnIkaB9e/giphy.gif)



**So what does it do?**

jQuery makes complicated things easier! A few examples... 
- It can dramatically simplfy DOM manipulation. 
- It allows you to hijack and handle events (ie. mouse click, double click, mouse hover).
- It makes AJAX (Asynchronous JavaScript and XML) easier to use.
- It enables the developer to create better, faster, and more interactive web applications. 



**How do I use it?**

Start by downloading it [here.](http://jquery.com/download/?)

Once you've followed the instructions on jQuery's website for downloading & installing, open up a project that includes some HTML. 

Then you'll need to remember three very important things. 

1.) jQuery always goes inside the 'Document Ready' script. This ensures that your program waits for the document to fully load before attempting to run any of the jQuery. 

<a href='https://postimg.cc/87gwvF2P' target='_blank'><img src='https://i.postimg.cc/87gwvF2P/document_ready.png' border='0' alt='document_ready'/></a>

(Shortcut: Instead of $(document).ready(function), you can use $(function).)

2.) Any time you want to reference jQuery, you need to begin by invoking the dollar sign, "$".

3.) When selecting an element in the code, you use a '#' selector just like in CSS.

Once you have selected a DOM element, you can change it at will using a large number of the jQuery manipulation methods. 

**Want to see some examples of jQuery methods?**

.hide()
.show()
.slideUp
.slideDown()
.delay()
.fadeToggle()
.CSS
.bind()
.unbind()
.live()
.die()

So many gadgets to play with! 

<iframe src="https://giphy.com/embed/OPOIcmwa6Ew2A" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/avengers-age-of-ultron-avengersedit-OPOIcmwa6Ew2A">via GIPHY</a></p>

The real superpower of jQuery comes from combining its abilities in **event handling**, **selection**, and **manipulation**.

An example:

$("#box1").on('click', function() {
     ("#box1).slideDown(500);
});

This would take whichever element is identified as box 1 and, upon it being clicked, would slide it down and out of sight over the course of 500 milliseconds. Wow! Easy! Helpful! 

And this is just one quick example of the many animations, selectors, methods, and manipulators that are available with jQuery. By adding this library to your programming repertoire, there are thousands of exciting combinations suddenly available to you! I have had a lot of fun learning the basics of jQuery and assimilating it into my programming. Do yourself a favor. Download it immediately, sit back, and be amazed at your newfound programming superpowers.

Welcome to the jQuery team! 

<iframe src="https://giphy.com/embed/103liSxCY1NpLO" width="480" height="183" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/iron-man-marvel-103liSxCY1NpLO">via GIPHY</a></p>


