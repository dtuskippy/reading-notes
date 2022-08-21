## Class-10 Reading Notes  
<p>Debugging is clearly always a relevant topic for any developer, especially me!  The JS call stack is extremely important to understand in terms of learning to structure the JS code base properly.</p>

### Understanding the JavaScript Call Stack

1. What is a ‘call’?
    * Function invocation, i.e. code that invokes the function to execute the code in its code block.
2. How many ‘calls’ can happen at once?
    * One.
3. What does LIFO mean?
    * When we say that the call stack operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be popped out, when the function returns.
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
    ```
    function add(a, b) {return a + b};
    function average(a, b) {return add(a, b) / 2;}
    let x = average(10, 20); // returns 15
    ```
    ![Call Stack](images/call-stack.png)

5. What causes a Stack Overflow?
    * A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

### JavaScript error messages

1. What is a ‘reference error’?
    * When a variable is used that is not defined yet.
2. What is a ‘syntax error’?
    * Like it says, improper syntax being used, e.g. leaving out the second curly brace for a function -- can be fixed by adding the second curly brace.
3. What is a ‘range error’?
    * Occurs when manipulating an object with some kind of length and you give it an invalid length (e.g. an array).
4. What is a ‘type error’?
    * E.g. attempt to access a property of an object that has not been defined yet.
5. What is a breakpoint?
    * When using a debugger tool (Google dev tools, VS Code, etc.), the breakpoint literally allows you to stop the code running at any point to inspect the code at a particular line of execution.
6. What does the word ‘debugger’ do in your code?
    * The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

## Things I want to know more about

1. I still have not had a chance to use the VS Code debugger, and that is something I need to find the time to work on.