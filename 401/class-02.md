# Class-02 Reading Notes

Node.js and Express are supposedly a review, but I still learned a lot reading some of the same materials again.  TDD and CD/CI are totally new to me, so look forward to digging into them with actual projects.

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

## [What is TDD?](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))

1. Explain why tests are important. Please explain as though I were your non technical elder.
    * Testing is important the same way testing an airplane or any manufactured prodcuct is important -- the final product is much less likely to fail if it has been tested throughout and following the design and build process.
2. What are three expected benefits of testing:
    * Reduction in defect rates.
    * Greater upfront overhead in TDD is more than offset by a reduction in fixing code in projects' final phases.
    * Industry veterans claim greater quality in code.
3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
    * Individual pitfalls:
      * Forgetting to run tests frequently.
      * Writing too many tests at once.
      * Writing tests that are too large or coarse-grained.
      * Writing overly trivial tests, for instance omitting assertions.
      * Writing tests for trivial code, for instance accessors.
    * Team pitfalls:
      * Partial adoption – only a few developers on the team use TDD.
      * Poor maintenance of the test suite – most commonly leading to a test suite with a prohibitively long running time.
      * Abandoned test suite (i.e. seldom or never run) – sometimes as a result of poor maintenance, sometimes as a result of team turnover.

## [CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)

1. What are three benefits of Continuous Integration?
    * Ensure everyone's changes integrate.
    * Catch bugs.
    * Reduce merge conflicts.
2. What is the difference between Continuous Delivery and Continuous Deployment?
    * Continuous Delivery: allows you to develop to release at any time.
    * Continuous Deployment: extension of continuous delivery;  allows you to deploy new feature immediately.
3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background.
    * GitHub serves as a clearing house that keeps track of changes in your code base, and also communicates with other systems about those changes with webhooks and APIs.

## Things I want to know more about

1. TDD and CI/CD are totally new to me, so look forward to actually working with these concepts on actual projects.
