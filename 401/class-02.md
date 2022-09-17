# Class-02 Reading Notes

As we enter the back-end world of web apps, clearly Node.js is a key topic to master for full stack JS apps.

## [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)

1. Explain middleware, answer as though I were a non-technical recruiter.
    * Similar to the role a language interpreter plays between two people unable to speak in a common language, middleware is the 'software glue' that allows different software apps, etc. to communicate and interconnect with each other.
2. Express is the most popular __ __ ____.
    * Node web framework.
3. Express is “unopinionated.” What does that mean?
    * *Opinionated frameworks* are those with opinions about the "right way" to handle any particular task. They often support rapid development in a particular domain (solving problems of a particular type) because the right way to do anything is usually well-understood and well-documented. However they can be less flexible at solving problems outside their main domain, and tend to offer fewer choices for what components and approaches they can use.
    * *Unopinionated frameworks*, by contrast, have far fewer restrictions on the best way to glue components together to achieve a goal, or even what components should be used. They make it easier for developers to use the most suitable tools to complete a particular task, albeit at the cost that you need to find those components yourself.
    * Express is unopinionated. You can insert almost any compatible middleware you like into the request handling chain, in almost any order you like. You can structure the app in one file or multiple files, and using any directory structure. You may sometimes feel that you have too many choices!
4. What is a module and why is modularity useful to us as developers?
    * A module is a JavaScript library/file that you can import into other code using Node's require() function. Express itself is a module, as are the middleware and database libraries that we use in our Express applications.
    * Individual developers can (and should, practically) create their own modules, and handle by exporting from the module itself and then having 'require()' to import it 'on the other side' (usually on the server.js file, from my limited experience) -- it is simply a type of coding paradigm (frankly, a concept used in most fields outside of comp sci as well) similar to componentization or micro-services -- just separating out blocks of code into identifiable parts where they are easier to work with, easier to organize, easier to detect errors, etc.

## [What is NPM?](https://docs.npmjs.com/about-npm)

1. What version of npm are you running on your machine?
    * 8.19.1
2. What command would you type to install a library/package called ‘jshint’ into your node project?
    * npm install -g jshint (this would install globally)
    * [JSHint described](https://en.wikipedia.org/wiki/JSHint)

## What is TDD?

1. Explain why tests are important. Please explain as though I were your non technical elder.
2. What are three expected benefits of testing
3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.

## CI/CD

1. What are three benefits of Continuous Integration?
2. What is the difference between Continuos Delivery and Continuous Deployment?
3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background


## Things I want to know more about

1. I would like to dig more into understanding the guts of Chrome's V8 JS Engine.
