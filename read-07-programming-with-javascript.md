## Programming with JavaScript

### Control Flow

* The control flow is the order in which the computer executes statements in a script.
* Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops.
* For example, imagine a script used to validate user data from a webpage form. The script submits validated data, but if the user, say, leaves a required field empty, the script prompts them to fill it in. To do this, the script uses a conditional structure or if...else, so that different code executes depending on whether the form is complete or not:

```
if (field==empty) {
    promptUser();
} else {
    submitForm();
}
```
* Control flow means that when you read a script, you must not only read from start to finish but also look at program structure and how it affects order of execution.
  
### Functions

* A JavaScript function is a block of code designed to perform a particular task.
* A JavaScript function is executed when "something" invokes it (calls it).
```
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}
```


### Operators

### JavaScript online resource

* Among many, probably the most respected practial online resource for developers is found [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript) on the MDN (Mozilla Developers Network) website.
