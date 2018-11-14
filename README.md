# How to Leverage JavaScript Events

## Learning Goals

* Define a JavaScript event
* Identify different types of user events
* Categorize JavaScript events

## Introduction

We've experimented with selecting and manipulate nodes in the DOM using
JavaScript: deleting nodes, editing nodes, etc. Web applications do work
like this in response to _events_ to communicate to application users that
something has changed (moved from "normal" status to "liked" status). So
a "click" _event_ might trigger the work to change a DOM element from green
to red.

In JavaScript we

1. Tell DOM nodes to "listen" for events...
2. ...and when they receive that event they "run" some amount of work
   stored in a _function_

In this lesson, we'll learn how to do just that. Don't worry if _functions_
are new to you. We'll cover them in greater depth once you've had a chance to
work with them.

## Define a JavaScript Event

JavaScript has event handlers that respond to user actions
such as mouse clicks, key presses, or window resizing. We can define code
that will be run when those events happen.

## Identify Different Types of User Events

Javascript gives us a few different event handlers that can be used.

### Mouse Click

Let's pretend we wanted to do something every time we click a certain element.
Here, we have a simplified code snippet that will turn the background of a
container with an id of `container` green.

Change to `addEventListener` – here and elsewhere.

```js
var container = document.querySelector("#container")

container.onclick = changeColorOnClick;

function changeColorOnClick(){
    container.style.backgroundColor = "green";
}
```

This code could also be easily modified to "toggle"--or switch back and forth,
between two colors.

### Key Press

Click events make up the majority of events you'll use, but other events you
might use include `keypress`, `keydown`, and `keyup`. These events have a
`which` property that tells us which key was pressed. Try it out by copying and
pasting the following in your JS console in the browser:

```js
var container = document.querySelector("#container")

container.onkeypress = changeColorOnKeyPress;

function changeColorOnKeyPress(){
    container.style.backgroundColor = "yellow";
}
```
This code snippet will change the color of the container with the id of `container`
to yellow on the event _any_ key being pressed. You can target specific keys with
this particular event, but we will be discussing `addEventListener` more later.

### Form Submission

HTML page usually uses a submit button to submit a form to a handling file, such
as a PHP script. All input values of the form will be transferred to the
handling file by `post` method. To submit a form to the server manually, we can
call `form.submit()`. There are a number of different ways to code JavaScript into
forms. We will be showing you one of many in future lessons.

## Categorize JavaScript Events

Event-handling code is not unique to JavaScript.
Most programming languages have some kind of event model. Your mobile device
knows how to detect screen slide events, device-shake events, and rotation events.

Even JavaScript for web is different from JavaScript in other
environments.

## Conclusion

(you've not intro'd functions yet, using "function call" is a cliff)

JavaScript allows us to do amazingly complex stuff when it detects events.

Common events are are 'scroll', 'mouseenter', 'mouseleave',
'focus', 'blur',  and 'onchange'. Learn these main events now, but 
scan the full list occasionally. As you seek to build more complicated applications,
you'll need to handle and trigger work on more events. Here's a list of a 
[ton of browser events](http://help.dottoro.com/larrqqck.php).

Speaking of triggering work, the work that handled events trigger is stored in
_functions_. It's time to dive deeply into this core element of the JavaScript language.


## Resources

- [MDN - Web Events][MDN]
- [StackOverflow - Bubbling and Capturing][SO]
- [QuirksMode - Event order][QM]

[instructions]: http://help.learn.co/workflow-tips/github/how-to-manually-open-a-lab
[help-center]: http://help.learn.co/the-learn-ide/common-ide-questions/viewing-html-pages-in-the-learn-ide
[MDN]: https://developer.mozilla.org/en-US/docs/Web/Events
[SO]: http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing
[QM]: http://www.quirksmode.org/js/events_order.html
