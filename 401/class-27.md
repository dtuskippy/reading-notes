# Class-27 useState() Hook

This is the topic of the week, and a pretty hot topic in React land.

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
    * They let you use state and other React features without writing a class.
2. When would I use the useState Hook?
    * useState is a Hook that lets you add React state to function components.
    * If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. 
    * Now you can use a Hook inside the existing function component.
3. If you were to add React state to a function component by declaring a state variable:
    * What does calling useState do?
        * It declares a “state variable”. 
        * Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. 
        * Normally, variables “disappear” when the function exits but state variables are preserved by React.
    * What do we pass to useState as an argument?
        * The only argument to the useState() Hook is the initial state. 
        * Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need.
        * In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)
    * What does useState return?
        * It returns a pair of values: the current state and a function that updates it.
        * This is why we write const [count, setCount] = useState(). 
        * This is similar to this.state.count and this.setState in a class, except you get them in a pair.

## Things I want to know more about

1. I need to know a LOT more about hooks -- plenty of learning to go, to put it mildly.