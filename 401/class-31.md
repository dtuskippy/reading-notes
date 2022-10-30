
# Class-31 Context API

This is the topic of the week, and a pretty hot topic in React land.

[Context API](https://reactjs.org/docs/context.html)

1. What can React Context provide your app?
    * Context provides a way to pass data through the component tree without having to pass props down manually at every level.
2. Why might we use Context?
    * Context is primarily used when some data needs to be accessible by many components at different nesting levels. 
3. Why should we use it sparingly?
    * Apply it sparingly because it makes component reuse more difficult.

[Awesome React Context links](https://github.com/diegohaz/awesome-react-context)

* Consume content from (at least) two of the Awesome React Context links. Share your take-away from each:
  * Takeaway 1: [Heres how React's New Context API Works by Wes Bos](https://www.youtube.com/watch?v=XLJN4JfniH4) 
    * Similar to Redux, Context attempts to deal with the problem of the complex nature of passing data down via props to parent to child in a serial nature -- it's pretty complex with a just few levels, but gets really complex as more and more levels added.
    * Redux is effectively a data store residing outside the app, where a dev can pull from to inject anywhere in an app.
    * Context attempts to do the same thing by wrapping an app in 'context' -- effectively creating an 'uber state' for an entire app, while still maintaining a parent-child data structure, with nomenclature for parent as 'producer', and 'consumer' for child.
  * Takeaway 2: [React's new context API: toggle between local and global state by Diego Haz](https://www.freecodecamp.org/news/reacts-new-context-api-how-to-toggle-between-local-and-global-state-c6ace81443d0)
    * We can break the new React Context API into three parts: Context, Provider and Consumer.
    * After creating context, we create our Provider, which uses Context.Provider and passes state and setState down.
    * And downstream, our Consumer needs to use Context.Consumer to access state and setState passed by Provider.
    * The final step is to wrap our app with Provider.

## Additional Questions

1. Looking ahead at this module’s course schedule, What do you look forward to learning?
    * Actually implementing with Context.
2. What are your learning goals after reading and reviewing the class README?
    * Short-term: just try to survive the materials this week, and long-term, have time to develop own project ideas so can dig much deeper into new and 'old' concepts.

## Things I want to know more about

1. I know we'll learn about Redux soon, so quite curious about how to decide on when to use these various Context with hooks versus Redux, etc.
