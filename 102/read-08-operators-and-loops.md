## Operators and Loops

### Operators 

* The most common and fundamental **assignment operator** is equal (=); an assignment operator assigns a value to its left operand based on the value of its right operand. 
  * E.g. x = "cats" assigns the value of the string, "cats", to the variable of x
* **Comparison operators** compare its operands and returns a logical value based on whether the comparison is true. The operands can be numerical, string, logical, or object values. 
  * Equal (==): Returns true if the operands are equal.
  * Not equal (!=): Returns true if the operands are not equal.
  * Strict equal (===): Returns true if the operands are equal and of the same type. 
  * Strict not equal (!==): Returns true if the operands are of the same type but not equal, or are of different type.	
  * Greater than (>): Returns true if the left operand is greater than the right operand.	
  * Greater than or equal (>=): Returns true if the left operand is greater than or equal to the right operand.	
  * Less than (<): Returns true if the left operand is less than the right operand.
  * Less than or equal (<=): Returns true if the left operand is less than or equal to the right operand.

### Loops

* When it comes to programming, few things are more fundamental than loops -- e.g. you wish to log  the numbers 1 through 5 to the console; instead of doing 5 separate console.log commands, a for loop can handle as such: 

```
for (let num = 1; num <= 5; num++) {
  console.log(num);
}
```
* **While loops** execute a specified statement as long as the test condition evaluates to true.

```
while (/*test condition*/) {
  /* specified statement */
}

const x = 1;
while (x <= 10) {
  console.log(x);
  x++;
}
```
* **For loops** create a loop that consists of three optional expressions:
  * initialization - An expression or variable declaration that evaluated once before the loop begins
  * condition - An expression to be evaluated before each loop iteration. If it evaluates to true, statement is executed
  * final-expression - An expression to be evaluated at the end of each loop iteration
* These expressions are enclosed in parentheses and separated by semicolons and are followed by a statement to be executed in the loop

```
for (/*initialization*/ ; /*condition*/ ; /*final-expression*/ ) {
  /* statement */
}

for (var x = 1; x <= 10; x++) {
  console.log(x);
}

```
### JavaScript online resource

* For operators, this is a great [resource](https://www.w3schools.com/js/js_operators.asp), and for loops, MDN has probably the best overview [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration).
