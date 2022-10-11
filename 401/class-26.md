# Class-26 Component Based UI

It's a topic that my team is considering for Lab 14, and a topic certainly relevant to Lab 19.  

## [react hello world](https://reactjs.org/docs/hello-world.html)

1. What are the building blocks of a React app?

    * React elements are the building blocks of React applications. One might confuse elements with a more widely known concept of “components”. An element describes what you want to see on the screen. React elements are immutable.
    * const element = <h1>Hello, world</h1>;
    * Typically, elements are not used directly, but get returned from components.
2. What is the difference between an element and a React component?

* React components are small, reusable pieces of code that return a React element to be rendered to the page. The simplest version of React component is a plain JavaScript function that returns a React element:

  ```
  
  function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
  }
  ```

* Components can also be ES6 classes:

```
  class Welcome extends React.Component {
    render() {
      return <h1>Hello, {this.props.name}</h1>;
    }
  }
  ```

3. What are some advantages of React’s component based architecture?

* Same advantage of any modularized architecture in coding or elsewhere:
  * Able to break the whole into manageable parts, making development, testing, security, and management among vast teams more easy.

## [introducing JSX](https://reactjs.org/docs/introducing-jsx.html)

1. What is JSX and why do we use it?
    * JSX is a syntax extension to JavaScript, and produce React elements.
2. Describe the process of embedding JavaScript expressions in JSX.
    * In the example below, a variable is declared and called name and then used inside JSX by wrapping it in curly braces:

    ```
    const name = 'Josh Perez';
    const element = <h1>Hello, {name}</h1>;
    ```

    * You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.
3. Is it safe to embed user input in JSX? Explain.
    * Yes, JSX prevents injection attacks

    ```
    const title = response.potentiallyMaliciousInput;
    // This is safe:
    const element = <h1>{title}</h1>;
    ```

    * By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered. This helps prevent XSS (cross-site-scripting) attacks.

## [rendering elements](https://reactjs.org/docs/rendering-elements.html)

1. Explain what a React Component is to a non-technical friend.
    * Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.
    * Like chapters in a book, they're both separate entities, but part of the greater whole.
2. Describe mutability and React Components, specifically, how is the UI updated?
    * React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
    * With our knowledge so far, the only way to update the UI is to create a new element, and pass it to root.render().
3. If changes are made to the UI, what does React update?
    * React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

## Bookmarks

1. [sass cheatsheet](https://devhints.io/sass)
2. [react cheatsheet](https://devhints.io/react)

## Things I want to know more about

1. My team is considering this topic for Lab 14, so planning to dig into the docs and dig further on youtube videos.
