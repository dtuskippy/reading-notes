## Class-5 Reading Notes  
<p>These are very JS-specific readings, and align well with planned labe as well as the continuing coding challenges.</p>

### Functional Programming Concepts

1. What is functional programming?
    * Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
2. What is a pure function and how do we know if something is a pure function?
    * It returns the same result if given the same arguments (it is also referred as deterministic)
    * It does not cause any observable side effects
    * Example was given of a function that calculates the area of circle (radius * radius * pi) -- if only the radius was set as a parameter and pi was left as a global variable, it would be considred impure, 'what if pi was changed some day by mathematicians someday' -- setting both radius and pi as parameters would make the function pure.
3. What are the benefits of a pure function?
    * The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
        * Given a parameter A → expect the function to return value B
        * Given a parameter C → expect the function to return value D
4. What is immutability?
    * When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
5. What is Referential transparency?
    * Passing 2 as a parameter of the square function will always returns 4. So now we can replace the square(2) with 4. That's it! Our function is referentially transparent.
    * Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
    * pure functions + immutable data = referential transparency

## Node JS Tutorial for Beginners #6 - Modules and require()
1. What is a module?
    * Rather than dump all the JS code in one bloated js file, the code is split up into separate files / modules based on its respective functionality, i.e. seems similar to component-based architecture of React / micro-services.
2. What does the word ‘require’ do?
    * Require is similar to import in React -- it's a way to effectively import another module's functionality into that particular file. -
3. How do we bring another module into the file the we are working in?
    * Example was given of a counter function in another file/module that was imported by the following code: const counter = require('./count'), i.e. ./count is file with a counter function. 
4. What do we have to do to make a module available?
    * Similar to React, the require call (specified in #3 above) only works if on the ./count side there is the following 'export' code: module.exports = counter;


## Things I want to know more about

1. I had read in the past very lightly about functional programming, and need to do some further reading on the topic to get my head full around the context of its practical use.
2. I clearly need reps to acquaint myself fully with modular programming.