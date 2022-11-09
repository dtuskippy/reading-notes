# Class-38 -- Redux - Asynchronous Actions

This is the topic of the week, and a pretty hot topic in React land.

## [async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)

1. Why use Redux middleware?
    * Redux middleware were designed to enable writing logic that has side effects.
    * A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function.
2. Consider the Redux Async Data Flow Diagram. Describe the flow in your own words.
    * Just like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.
    * Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.
    * Earlier, we saw a diagram that represents the normal synchronous Redux data flow. When we add async logic to a Redux app, we add an extra step where middleware can run logic like AJAX requests, then dispatch actions.
3. How are we accommodating async in our Redux app?
    * By using middleware, namely thunk middleware.

## [thunk middleware](https://github.com/reduxjs/redux-thunk)

1. Why would you need redux-thunk middleware?
    * With a plain basic Redux store, you can only do simple synchronous updates by dispatching an action. Middleware extends the store's abilities, and lets you write async logic that interacts with the store.
2. Redux Thunk middleware allows you to write action creators that return a ____ instead of an action.
    * Redux Thunk middleware allows you to write action creators that return a function instead of an action.
3. Describe how any return value from the inner thunk function will be made available.
    * Any return value from the inner function will be available as the return value of dispatch itself.

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    * Learning about Redux middleware, specifically React Thunk.

## Things I want to know more about

1. Redux is a complex topic I have barely scratched the surface of, so plenty more to dig into.