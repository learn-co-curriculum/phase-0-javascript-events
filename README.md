# How to Leverage JavaScript Events

## Learning Goals

* Define a JavaScript event
* Identify different types of user events
* Categorize JavaScript events

## Introduction

We've experimented with selecting and manipulate nodes in the DOM using
JavaScript. We've also experimented with creating and removing elements.
Wouldn't it be more interesting if we made those types of thing happen
when we did something—such as clicked on an element, pushed a button,
or moved our mouse? Those actions are called "events." In JavaScript we
can "listen" for events and use them to call functions that update the
DOM. In this lesson, we'll learn how to do just that.

## Define a JavaScript Event

JavaScript has event handlers that respond to user actions—user actions
such as mouse clicks, key presses, or window resizing. We can define code
that will be run when those events happen.

JavaScript allows us to bind—or connect—functions to particular events. We
create a function, and then tell the browser to run that function whenever that
event happens.

## Identify Different Types of User Events

Javascript gives us a few different event handlers that can be used.

### Mouse Click

Let's pretend we wanted to do something every time we click a certain element.
Here, we have a simplified code snippet that will turn the background of a
container with an id of `container` green.

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

It is important to note that web events are not part of the core JavaScript
language—they are defined as part of the JavaScript APIs built into the browser.
This means that different browsers can often support different sets of events, or
have different names for them.

Another thing worth mentioning is that events are not particular to JavaScript.
Most programming languages have some kind of event model which will often differ
from JavaScript. Even JavaScript for web is different from JavaScript in other
environments.

For example, Node.js enables developers to use JavaScript to build network and
server-side applications. It doesn't sound different, but the code _is_ quite
different. You can also use JavaScript to build cross-browser add-ons with
WebExtensions.

You don't need to understand other environments just yet, but these are some
examples to illustrate that JavaScript events can vary. Don't be alarmed when
you come across those differences in the future.

## Conclusion

JavaScript allows us to do amazingly complex stuff with a simple function call.
Now that you have been given the basics of events to get started, you can explore
more event handlers! Here's a list of a 
[ton of browser events](http://help.dottoro.com/larrqqck.php).

Some other common events are are 'scroll', 'mouseenter' and 'mouseleave',
'focus', 'blur',  and 'onchange'. There are lots and lots of events - what
events do popular websites handle? This might feel intimidating at first, but if
you familiarize yourself with them all now, you can get the hang of using them
before you end up needing them for a project task!

## Resources

- [MDN - Web Events][MDN]
- [StackOverflow - Bubbling and Capturing][SO]
- [QuirksMode - Event order][QM]

[instructions]: http://help.learn.co/workflow-tips/github/how-to-manually-open-a-lab
[help-center]: http://help.learn.co/the-learn-ide/common-ide-questions/viewing-html-pages-in-the-learn-ide
[MDN]: https://developer.mozilla.org/en-US/docs/Web/Events
[SO]: http://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing
[QM]: http://www.quirksmode.org/js/events_order.html
