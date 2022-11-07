
# Class-36 -- Application State with Redux

This is the topic of the week, and a pretty hot topic in React land.

## [Dan Abramov Redux Tutorials](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)

1. What is the first principle of Redux?
    * Representing all state in an app in a single JavaScript object.
2. What is a store and what do we use our reducers for within that store?
    * The store is a “container” (really a JavaScript object) that holds the application state, and the only way the state can change is through actions dispatched to the store. 
    * Redux allows individual components to connect to the store and apply changes to it by dispatching actions.
    * The reducers are the pure functions that contain the logic and pure calculations that are needed to be performed on the state.
      * These functions accept the initial state of the state being used and the action type. 
      * It updates the state and responds with the new state.
3. Name three Redux store methods given to us by createStore and describe their use.
    * getState()
      * Returns the current state tree of your application. It is equal to the last value returned by the store's reducer.
    * dispatch() 
      * The only way to update the state is to call store.dispatch() and pass in an action object.
    * subscribe()
      * Adds a change listener. It will be called any time an action is dispatched, and some part of the state tree may potentially have changed. You may then call getState() to read the current state tree inside the callback.
4. Explain to a non-technical recruiter what combineReducers() does and why it is useful.
    * The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

## Bookmarks

1. [World's easiest guide to Redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)
2. [Testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)
3. [Redux Docs](https://redux.js.org/)

## Things I want to know more about

1. Good review on things we have already covered, but a complex topic I have barely scratched the surface of, so plenty more to dig into.

##  Questions

1. Looking ahead at this module’s course schedule, What do you look forward to learning?
    * I look forward to learning about Redux.
2. What are your learning goals after reading and reviewing the class README?
    * To try learn as much about Redux as is reasonable in a matter of days.