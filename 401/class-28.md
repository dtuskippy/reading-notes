# Class-28 useEffect() Hook

This is the topic of the week, and a pretty hot topic in React land.

## [effects hook](https://reactjs.org/docs/hooks-effect.html)

1. What purpose does useEffect serve in a function component compared to its counterpart(s) in class components?
    * If you’re familiar with React class lifecycle methods, you can think of useEffect Hook as componentDidMount, componentDidUpdate, and componentWillUnmount combined.
2. When using the useEffect Hook:
    * What does useEffect do?
        * By using this Hook, you tell React that your component needs to do something after render.
        * React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. 
        * In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.
    * Why is useEffect called inside a component?
        * Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect.
        * We don’t need a special API to read it — it’s already in the function scope. 
        * Hooks embrace JavaScript closures and avoid introducing React-specific APIs where JavaScript already provides a solution.
3. Explain the importance of properly implementing effects with Cleanup.
    * For example, we might want to set up a subscription to some external data source. In that case, it is important to clean up so that we don’t introduce a memory leak! Let’s compare how we can do it with classes and with Hooks.

## Things I want to know more about

1. This is my absolute first intro useEffect, so plenty to still learn about it.