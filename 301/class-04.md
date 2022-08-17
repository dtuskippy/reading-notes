## Class-4 Reading Notes  
<p>The topic of component-based architecture relates directly to beginning to work with React.</p>

### React Docs - Forms

1. What is a ‘Controlled Component’?
    * An input form element whose value is controlled by React is called a “controlled component”.
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
    * You can do either -- depends on the use case and what the goal is of the app.
3. How do we target what the user is entering if we have an event handler on an input field?
    * When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

### The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
    * Shortens conditional code blocks.
2. Rewrite the following statement using a ternary statement:
    * x === y ? console.log(true) : console.log(false)

## Things I want to know more about

1. I still need more work fully understanding state.