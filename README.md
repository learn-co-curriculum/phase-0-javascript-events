# How to Leverage JavaScript Events

## Learning Goals

* Define a JavaScript event
* Identify different types of user events
* Categorize JavaScript events

## Introduction

We've experimented with selecting and manipulate nodes in the DOM using
JavaScript: deleting nodes, editing nodes, etc. But most web applications are
not used by people opening up the console and editing the DOM directly :).
Instead, people _do something_ and then _work happens_.

In JavaScript we tell DOM Nodes to "listen" for someone "doing something." This
is called an "event." In the "Simple Liker" application we're listening for
someone to "click on the heart icon." In response to someone _doing something_,
JavaScript "does work." In JavaScript we bundle work, like what we learned to
do in the JavaScript console, inside a holder of work called a "function."
We'll explore functions and how to write them shortly, but for the moment you
can think of them as a way to define work, _but not do it_..._yet_.

Listening for events and triggering work when they're "noticed" is called
"event handling."

## Define a JavaScript Event

JavaScript has the ability to "listen" on DOM nodes to whether an "event"
happens to that node. The simplest is "click." By setting up an "event
listener" on a DOM node, we're halfway to having "handled the event." We'll
cover a few more common types of events below.

## Identify Different Types of User Events

JavaScript gives us a few different event handlers that can be used.

### Mouse Click

Let's pretend we wanted to do something every time we click a certain element.
Here, we have a simplified code snippet that will turn the background of a
container with an id of `container` green.

KELLYE: Change to `addEventListener` – here and elsewhere.

```js
var container = document.querySelector("#container")

container.onclick = changeColorOnClick;

function changeColorOnClick(){
    container.style.backgroundColor = "green";
}
```

This code could also be easily modified to "toggle"--or switch back and forth,
between two colors. The mouse is a primary user interface tool for web sites:
handling these pointer device (mouse, finger) events is a skill you must
master.

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

This code snippet will change the color of the container with the id of
`container` to yellow on the event _any_ key being pressed. If ever you want to
make a browser-based game, you're going to want to be comfortable with handling
key events.

### Form Submission

HTML pages often use a submit button to submit a form to a server.  All
`<input>` values of the `<form>` will be transferred to the server. When a user
submits a form, the `submit` event is fired. An event handler here might pop up
a thank you overlay, play a song, or provide some other sort of interactivity.

### List of Events

As you seek to build more complicated applications, you'll need to handle and
trigger work on more events. Here's a list of a [ton of browser
events][list].

## Categorize JavaScript Events

Event-handling code is not unique to JavaScript.  Most programming languages
have some kind of event model. Your mobile device knows how to detect screen
slide events, device-shake events, and rotation events.

## Conclusion

JavaScript allows us to trigger work when it detects events.  Common events are
are 'scroll', 'mouseenter', 'mouseleave', 'focus', 'blur', and 'onchange'.
When JavaScript recognizes an event that applies to a "event handler" that has
been set up, it will execute that "handler's" work, which is stored in a
function. While you've seen `function`s in this lesson, we'll make a deep dive
into them in the next lesson.

## Resources

- [MDN - Web Events][MDN]
- [StackOverflow - Bubbling and Capturing][SO]
- [QuirksMode - Event order][QM]

[instructions]: http://help.learn.co/workflow-tips/github/how-to-manually-open-a-lab
[help-center]: http://help.learn.co/the-learn-ide/common-ide-questions/viewing-html-pages-in-the-learn-ide
[MDN]: https://developer.mozilla.org/en-US/docs/Web/Events
[SO]: http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing
[QM]: http://www.quirksmode.org/js/events_order.html
[list]: http://help.dottoro.com/larrqqck.php
