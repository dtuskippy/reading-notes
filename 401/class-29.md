
# Class-29 Advanced State with Reducers

This is the topic of the week, and a pretty hot topic in React land.

## [useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer)

1. Name an alternative to the useState Hook.
    * useReducer.
2. Why might the useReducer Hook be preferable to the useState Hook?
    * useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.
    * useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
3. What are two ways to set the initial state?
    * The simplest way is to pass the initial state as a second argument:

    ```
    const [state, dispatch] = useReducer(
      reducer,
      {count: initialCount}
    );
    ```

      * React doesn’t use the state = initialState argument convention popularized by Redux. The initial value sometimes needs to depend on props and so is specified from the Hook call instead. If you feel strongly about this, you can call useReducer(reducer, undefined, reducer) to emulate the Redux behavior, but it’s not encouraged.
    * Lazy initialization
      * You can also create the initial state lazily. To do this, you can pass an init function as the third argument. The initial state will be set to init(initialArg).

## [Ultimate Guide to useReducer](https://blog.logrocket.com/react-usereducer-hook-ultimate-guide/)

1. In terms of state, what does useReducer expect to receive as a parameter?
    * It accepts a reducer function as its first parameter and the initial state as the second.
2. What does useReducer return?
    * useReducer returns an array that holds the current state value and a dispatch function to which you can pass an action and later invoke it. While this is similar to the pattern Redux uses, there are a few differences.
3. Explain dispatch to a non-technical recruiter.
    * The dispatch function accepts an object that represents the type of action we want to execute when it is called. 
    * Basically, it sends the type of action to the reducer function to perform its job, which, of course, is updating the state.

## Things I want to know more about

1. I know we'll learn about Redux soon, so quite curious about how gto decide on when to use these various hooks, etc.
