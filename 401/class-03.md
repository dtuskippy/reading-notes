# Class-03 Reading Notes

Express Router is new material re. the backend for me.

## [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

1. Classes are a template for creating ____.
    * Classes are a template for creating objects.
    * They encapsulate data with code to work on that data.
    * Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.
2. Can a class declaration be hoisted?
    * Evidently, technically, yes, but practically no.
      * Classes are hoisted but their values are not initialized.
      * So, an important difference between function declarations and class declarations is that while functions can be called in code that appears before they are defined, classes must be defined before they can be constructed.
3. How would you describe a constructor and contextual “this” to a non-technical friend?
    * *this* simply refers to the properties and methods within that specific class or constructor, i.e. *this* means this.

## [Using Express Routing](https://expressjs.com/en/guide/routing.html)

1. Within Express, what does routing refer to?
    * Routing refers to how an application’s endpoints (URIs) respond to client requests.
2. What is the difference between a route path and a route method?
    * Route method: A route method is derived from one of the HTTP methods, and is attached to an instance of the express class, e.g. app.get() or app.post().
    * Route path: Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.  E.g. This route path will match requests to /about with an app.get() method: '/about'.
3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?
    * With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.

## [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)

1. What is an Express Router?
    * Router is like a mini-Express application. It doesn’t bring in views or settings but provides us with the routing APIs like .use, .get, .param, and route.
2. By what mean do we initialize express.Router() in an express server?
    * // get an instance of router: let router = express.Router();
3. What do we use route middleware for?
    * Route middleware in Express is a way to do something before a request is processed.
    * This could be things like checking if a user is authenticated, logging data for analytics, or anything else we’d like to do before we actually spit out information to our user.

## Things I want to know more about

1. Express router seems understandable at first glance, but I need to dig into it code-wise and understand it better from the conceptual side.