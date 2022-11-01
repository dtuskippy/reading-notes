
# Class-32 Context API -- Behaviors

This is the topic of the week, and a pretty hot topic in React land.

## [Hooks and Context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)

1. With regard to the React Context API, what does a “provider” do?
    * Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.
    * The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.
2. With regard to the React Context API, how would we implement a “consumer” role?
    * A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.
3. Specifically with Context, how are we “wrapping” components to achieve our goals?
    * The Context provider is wrapped around the app, and all components in the app are then able to access the upstream state.

## [Awesome React Context links](https://github.com/diegohaz/awesome-react-context)

Consume content from (at least) two more of the Awesome React Context links. After some familiarity with React Context, once again share your takeaways from each:

* Takeaway 1: [Replacing redux with the new React context API by Didier FRANC](https://medium.com/@DidierFranc/replacing-redux-with-the-new-react-context-api-8f5d01a00e8c)
  * Effectively gives a comparison showing that Context with hooks is roughly equivalent to Redux in terms of functionality / performance.

* Takeaway 2: [React v16.3.0: New lifecycles and context API by Brian Vaughn (official)](https://reactjs.org/blog/2018/03/29/react-v-16-3.html)
  * In React v16.3.0, StrictMode is a tool for highlighting potential problems in an application, and helps with, identifying components with unsafe lifecycles, warning about legacy string ref API usage, and detecting unexpected side effects.

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    * Try to gain a deeper understanding of the fundamentals of working with React Context.

## Things I want to know more about

1. I know we'll learn about Redux soon, so quite curious about how to decide on when to use Context with hooks versus Redux, etc.
