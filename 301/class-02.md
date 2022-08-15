## Class-2 Reading Notes  
<p>The topic of the react lifecycle and state/props is fundamental to getting my head around React.</p>

### React Lifecycle

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
    * 'Render' happens first.
2. What is the very first thing to happen in the lifecycle of React?
    * Mounting.
3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
    * constructor
    * render
    * React Updates
    * componentDidMount
    * componentWillUnmount
4. What does componentDidMount do?
    * It is invoked immediately after a component is mounted.
    * Anything using a network request or initializing the DOM should go here, and it is a good place to set up any subscriptions.

### React State Vs Props

1. What types of things can you pass in the props?
    * Props are passed to components similar to the way arguments are passed to functions, i.e. data in the form of objects, etc.
2. What is the big difference between props and state?
    * Props are passed into components from outside the component, whereas state is handled within a component.
3. When do we re-render our application?
    * When there is a change of state within the component.
4. What are some examples of things that we could store in state?
    * The best example given was a counter component, where the initial count was passed to the component as a prop, but the subsequent counter continually updated inside the component, i.e. the counter variable inside the component is the example of something that can be stored in state.

## Things I want to know more about

1. I am still very much trying to get my head around all things React.  I will have to do a lot of reps to get comfortable with it.