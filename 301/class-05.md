## Class-5 Reading Notes  
<p>The React Docs topic seems super relevant and deals with the subjectivity required to actually architect (for lack of a better term) a React app, where hard decisions are required about fuzzy situations about when to make break out a component into sub-components and where to store state. Higher-order functions are of course relevant, as they describe key concepts in JS.</p>

### React Docs - Thinking in React

1. What is the single responsibility principle and how does it apply to components?
    * When deciding on what is a component and what will not be a component (effectively the process of how to structure/categorize data/data processing), the single responsibility principle is a rule-of-thumb that states that a component should ideally only do one thing.
2. What does it mean to build a ‘static’ version of your application?
    * Conceptually it's a 'first draft' approach, where you keep things simple by eliminating interactivity and any use of state, and stick to building the data model and rendering the UI.
3. Once you have a static application, what do you need to add?
    * Now you move to adding interactivity to your UI with a minimal amount of state.
4. What are the three questions you can ask to determine if something is state?
    * Is it passed in from a parent via props? If so, it probably isn’t state.
    * Does it remain unchanged over time? If so, it probably isn’t state.
    * Can you compute it based on any other state or props in your component? If so, it isn’t state.
5. How can you identify where state needs to live?
    * Identify every component that renders something based on that state.
    * Find a common owner component (a single component above all the components that need the state in the hierarchy).
    * Either the common owner or another component higher up in the hierarchy should own the state.
    * If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

### Higher-Order Functions

1. What is a “higher-order function”?
    * Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.
2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
    * Setting up a boolean that will return true if m > n, with n being the parameter.
3. Explain how either map or reduce operates, with regards to higher-order functions.
    * The map method transforms an array by applying a function to all of its elements and building a new array from the returned values. The new array will have the same length as the input array, but its content will have been mapped to a new form by the function.
    * Reduce computes a single value from an input array. Reduce builds a value by repeatedly taking a single element from the array and combining it with the current value. When summing numbers, you’d start with the number zero and, for each element, add that to the sum.

## Things I want to know more about

1. Specific to 'Thinking in React', I am curious about how often significant changes occur to React architecture in the real world, especially for a fast growing company, which may not only be adding whole new product categories with different requirements, but even a new business model, where, e.g. a product company moves to subscription -- basically, I'm curious how 'disruptive' the disruptive company is to itself in terms of web app architecture.