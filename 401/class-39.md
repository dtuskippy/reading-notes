# Class-39 -- Redux - Additional Topics

This is the topic of the week, and a pretty hot topic in React land.

## [Redux Toolkit (RTK)](https://redux-toolkit.js.org/introduction/getting-started)

1. What concerns are addressed by Redux Toolkit?
    * "Configuring a Redux store is too complicated."
    * "I have to add a lot of packages to get Redux to do anything useful."
    * "Redux requires too much boilerplate code."
2. What does configureStore() do?
    * Wraps createStore to provide simplified configuration options and good defaults. 
    * It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
3. How would I use createSlice()?
    * Accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.

## [MobX](https://mobx.js.org/getting-started.html)

1. What is Mobx?
    * MobX is a simple, scalable and battle tested state management solution. 
2. How does MobX make it “impossible” to produce an inconsistent state?
    * The strategy to achieve that is simple: Make sure that everything that can be derived from the application state, will be derived. Automatically.
3. How would we build a reactive user interface?
    * The observer HoC wrapper from the mobx-react-lite package fixes that by basically wrapping the React component in autorun.

## [Tutorial](https://redux-toolkit.js.org/tutorials/overview)

1. What take-away(s) did this tutorial provide?
    * It briefly shows how to add and use Redux Toolkit in a React application.

## Bookmarks

1. [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
2. [HookState](https://hookstate.js.org/)

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    * To get acquainted with alternate Redux store managers, like Ducks and Redux Tookit, and other ways to manage state, namely with MobX.

## Things I want to know more about

1. Redux is a complex topic I have barely scratched the surface of, so plenty more to dig into.