# JavaScript Events

## Learning Goals

* Define a JavaScript event
* Define event handling
* Identify different types of user events

## Introduction

In Software Engineering Prep, you learned how to select and manipulate nodes in
the DOM using JavaScript: deleting nodes, editing nodes, etc. But most web
applications are _not_ used by people opening up the console and editing the DOM
using Chrome's DevTools. Instead, people _do something_ (e.g., click a button)
and then _work happens_ (e.g., a form opens, or the number of likes on an image
increases by one).

Writing application code that "does some work" in response to "something
happening" is known as _event handling_. _Events_ are the "something the user
does" and the "_callback function_" is the work that will happen when the event
is triggered.

In the next few lessons, we'll learn what types of JavaScript events our code
can listen for, how to set up an _event listener_ to recognize an event, and how
to implement callback functions to handle the "work happens" part of event
handling. In this lesson, we'll start by learning more about what events are and
then we'll introduce some of the most common event types that JavaScript can
listen for.

## Define JavaScript Events

An event is simply an action of some type that occurs within the browser window
that JavaScript can "listen" for. Many events are the result of some type of
user action, for example, clicking some element on the page, submitting a form,
etc. However, there are many other events that are not the direct result of a
user action. Some examples include errors when loading an image or other
resource, a notification that the DOM has fully loaded, or an indication that a
video or other type of media is ready to play. JavaScript can "listen" for any
of these types of events — and [many others][list] — and as developers we can
use this capability to create interactive web applications and improve our
users' experience.

Let's take a look at a few of the most common types of events.

### Mouse Click

Mouse or trackpad events are some of the most common ones you'll be handling
with JavaScript. For example, JavaScript can recognize a single click
on an element in the page and change the styling of the element to highlight it.
Or it can recognize a double-click on an element and open a zoomed-in view of
that element.

There are many other mouse events you can use; take a look at the list of
JavaScript's [mouse events here][mouse].

### Key Press

While click events will likely make up the majority of events you'll use, the
keyboard is another important source of events. JavaScript currently includes
two [keyboard events][keyboard]: `keydown` and `keyup`. (A third, `keypress`,
has been deprecated.) When a key is pressed, these events provide a code to
indicate which key it was. For example, a game program might listen for
`keydown` events and, if the right arrow was pressed, make the character move to
the right.

### Form Submission

HTML pages often use a submit button to submit a form to a server. When a user
submits a form, the `submit` event is fired. An event handler here might pop up
a thank you overlay or log in the user and take them to their home page.

### Other Events

As you seek to build more complicated applications, you'll need to handle and
trigger work on many more events than the few we've discussed in this lesson.
Some other common events you are likely to encounter are `scroll`, `mouseenter`
and `mouseleave`, `focus`, `blur`,  and `change`.

## Event Handling Example

Let's use the example of clicking a "like" button to illustrate the process of
handling a JavaScript event:

1. When the application loads, JavaScript code is executed that:

   a. accesses the "like" button in the HTML using DOM query methods, and

   b. adds an event listener to it.

   The event listener takes two arguments: the event to listen for (in this
   case, "click") and a callback function.

2. When the user clicks the "like" button, the event listener calls the callback
   function.
3. The callback function performs some action or actions, e.g., updating the DOM
   to reflect the new number of likes.

We will cover each of these steps in the next few lessons.

## Conclusion

JavaScript allows us to trigger work when it detects events. You set up an event
handler and, when JavaScript recognizes that event, it will execute the event
handler's work, which is stored in a _callback function_.

Take a few minutes to look through the [list of common DOM events][list] to
familiarize yourself with the many many ways you can use event handling to
enhance your users' experience.

## Resources

* [MDN - Web Events][MDN]
* [MDN - Mouse Events][mouse]
* [MDN - Keyboard Events][keyboard]

[mouse]: https://developer.mozilla.org/en-US/docs/Web/API/Element#mouse_events
[keyboard]: https://developer.mozilla.org/en-US/docs/Web/API/Element#keyboard_events
[list]: https://www.w3schools.com/jsref/dom_obj_event.asp
[MDN]: https://developer.mozilla.org/en-US/docs/Web/Events
