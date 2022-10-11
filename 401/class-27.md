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
2. How would you identify a custom Hook and why might you create one?

## [the state hook](https://reactjs.org/docs/hooks-state.html)

1. What is a Hook?
2. When would I use the useState Hook?
3. If you were to add React state to a function component by declaring a state variable:

    * What does calling useState do?
    * What do we pass to useState as an argument?
    * What does useState return?

## Things I want to know more about

1. My team is considering this topic for Lab 14, so planning to dig into the docs and dig further on youtube videos.