# Class-27 useState() Hook

It's a topic that my team is considering for Lab 14, and a topic certainly relevant to Lab 19.  

## [Introducing Hooks](https://reactjs.org/docs/hooks-intro.html#motivation)

1. What was the motivation for introducing Hooks?
    * They let you use state and other React features without writing a class.
    * It’s hard to reuse stateful logic between components.
    * Complex components become hard to understand.
    * Classes confuse both people and machines.
2. What changes are important regarding implementing Hooks versus Component Classes?
    * Crucially, Hooks work side-by-side with existing code so you can adopt them gradually.
    * There is no rush to migrate to Hooks.
    * They recommend avoiding any “big rewrites”, especially for existing, complex class components.
3. Hooks allow you to reuse stateful logic without changing ___ _______.
    * With Hooks, you can extract stateful logic from a component so it can be tested independently and reused.
    * Hooks allow you to reuse stateful logic without changing your *component hierarchy*. 
    * This makes it easy to share Hooks among many components or with the community.

## [hooks api](https://reactjs.org/docs/hooks-overview.html)

1. Name two rules imposed by React Hook usage.
    * Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
    * Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment.)
2. How would you identify a custom Hook and why might you create one?
    * If a function’s name starts with ”use” and it calls other Hooks, we say it is a custom Hook. 
    * You can write custom Hooks that cover a wide range of use cases like form handling, animation, declarative subscriptions, timers, and probably many more we haven’t considered

## [the state hook](https://reactjs.org/docs/hooks-state.html)

1. What is a Hook?
2. When would I use the useState Hook?
3. If you were to add React state to a function component by declaring a state variable:

    * What does calling useState do?
    * What do we pass to useState as an argument?
    * What does useState return?

## Things I want to know more about

1. My team is considering this topic for Lab 14, so planning to dig into the docs and dig further on youtube videos.