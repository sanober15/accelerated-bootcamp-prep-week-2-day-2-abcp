# Week 3, Day 2
Today, we'll learn how to use jQuery to modify HTML and build an interactive webpage. We'll conclude by building an interactive in-browser game!

# What is jQuery

jQuery is a light-weight JavaScript library that allows us to write JavaScript more easily.

It wraps up a lot of the verbose functionality of JavaScript into simple, semantic functions.

We need to include the jQuery library in our project in order to use it.

One way to do so is via the Google CDN. Add the following to your index.html

```html
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3/jquery.min.js"></script>
```

# Using jQuery to Manipulate HTML

We can write jQuery in our HTML files inside `<script></script>` tags. We place those tags at the bottom of the HTML page so that it runs after our page loads.

```javascript
$("#yo").append("hey hey hey hey!!!!!”);

// jQuery.selector.function(argument)
```

The $ is just a function — it's equivalent to jQuery (which is also a function that you can call). You might think of it as a fancy alias (with a few tricks up its sleeve) to document.querySelectorAll.

"#yo" is our jQuery selector -- we're selecting the HTML element with the ID “yo”.
Then we use the jQuery append function, which adds text to an HTML element.

We pass that function an argument of, "hey hey hey hey!!!!!".

# Document Ready
So far, we’ve written our JavaScript code directly in our HTML file.
However, we hate this approach (it’s okay, you can admit how much it made your skin crawl).
Combining our code like this is messy and confusing and once you start writing longer JavaScript programs to interact with the DOM, it will get really ugly, really fast.

If our JS code is in a separate file from our HTML code, how do we:
1. Load the JS file?
2. Ensure our JS code runs only after the HTML page loads?

```javascript
$(document).ready(function() {
  // code to be executed goes here
});
```

The $ is a shortcut for jQuery, and provides an interface to the library. Every time you see $, think jQuery.

We are adding an event listener to the document for the load, or ready, event.
When the load event occurs for the document, execute the code in our callback function.
The body of the callback function will contain all of the jQuery code we want to use on our page.

# jQuery Selectors

jQuery lets us use HTML selectors to easily select the element we want to work with.
We wrap these selectors in a call to the $, or jQuery, function, for example $(“div”)
Open up the jQuery Selectors Lab and open the index.html file in your browser

# jQuery Event Listeners
Ever used a website where an action you took triggered something to happen on the page? You clicked part of a form and suddenly more to fill out appeared. You moused over part of the page and a modal window appeared. On Facebook, you click to see more comments and the rest appear. The list goes on and on and on. When these actions happen, code is responding to an event taken by a user, and responding with an action.

In JavaScript, these things that happen are called DOM events and the code written to trigger the action is called an event listener or event handler.

# Final Project: Rock Dodger
