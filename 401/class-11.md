# Class-11 Reading Notes

We already learned some event-driven programming on the frontend, and now we learn about the same concept on the backend.

## [Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)

1. What native Node.js module allows us to get started with Event Driven Programming?
    * [Event Emitter](https://nodejs.org/api/events.html#events_class_eventemitter).
2. What is the value of Object Oriented Programming used in tandem with Event Driven Programming?
    * Rather than on object needing to reach inside another object to trigger a function, objects can just emit events and whichever objects are listening to those events will process it in the way they have been told to.
    * The source of an object's behavior is now entirely contained within itself, rather than needing to be accessed by external objects.
3. Consider your knowledge of Event Driven Programming in the Web Browser, now explain to a non-technical friend how Event Driven Programming might be useful on the backend using Node.js.
    * With a web browser, an event can be clicking an image or clicking submit on a form.
    * Similarly on the backend, an event can be the login of a user that triggers certain actions.

## Bookmarks

1. [Node docs: events](https://nodejs.org/api/events.html)

## Things I want to know more about

1. It would be good to find the time to dig into the Node.js events documentation.