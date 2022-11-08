# Class-37 -- Redux - Combined Reducers

This is the topic of the week, and a pretty hot topic in React land.


## [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)

1. Why create multiple reducers?
    * Because it will be a mess to maintain a single gigantic reducer..
2. How would you combine multiple reducers?
    * To manage multiple reducers there is a function called combineReducers in the redux.
    * This basically helps to combine multiple reducers into a single unit and use them.
3. How will you manage state as an immutable object? why?
    * You never want to mutate the state.
   
## [Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)

1. combineReducers is a utility function to simplify the most common use case when writing ___ _____ .
    * Redux reducers.
2. Explain how combineReducers assembles the new state tree.
    * In order to assemble the new state tree, combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. 
    * So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.
3. How would you define initial state in an app using combineReducers?
    * combineReducers takes an object full of slice reducer functions, and creates a function that outputs a corresponding state object with the same keys.
    * This means that if no preloaded state is provided to createStore, the naming of the keys in the input slice reducer object will define the naming of the keys in the output state object.
    * The correlation between these names is not always apparent, especially when using ES6 features such as default module exports and object literal shorthands.

## [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)

1. Why will you want to split your reducing functions as your app becomes more complex?
    * As your app grows more complex, you'll want to split your reducing function into separate functions, each managing independent parts of the state.
2. The _____ helper function turns an object whose values are different reducing functions into a single reducing function you can pass to ____.
    * The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.
3. What is a popular convention when naming reducers?
    * A popular convention is to name reducers after the state slices they manage, so you can use ES6 property shorthand notation: combineReducers({ counter, todos }). 
    * This is equivalent to writing combineReducers({ counter: counter, todos: todos }).

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    * To gain a basic intro to Redux reducers.

## Things I want to know more about

1. Redux is a complex topic I have barely scratched the surface of, so plenty more to dig into.