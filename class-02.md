## Class-02 Reading Notes  
<p>It is pretty self-evident that readings on HTML, CSS and JavaScript have relevance to the course at hand -- they're the building blocks of modern websites.</p>

### HTML Text Fundamentals; HTML Advanced Text Formatting

1. Why is it important to use semantic elements in our HTML?
    * People are used to standards for written documents, be they newspapers, books, or web pages -- i.e. users viewing a website find it much easier to read and navigate a website if the website adheres to generally accepted standards like headings and paragraphs with line breaks, etc. 
    * Search engines rely on standardized html elements to quickly make sense of websites, and gauge their relevance.
    * Screen readers rely on standardized html elements, and can read headings to visually impaired people so they do not have to listen to a read-out of the entire web page before deciding on where they have interest to dive deeper.
    * CSS relies heavily on targeting standardized html elements for styling.
2. How many levels of headings are there in HTML?
    * There are 6 levels of headings in HTML.
3. What are some uses for the < sup > and < sub > elements?
    * A great use case example of the < sup > element is for dates like the twenty sixth of August, e.g. 26<sup>th</sup> of August.
    * A great use case example of < sub > element is for a chemical formula, e.g. H<sub>2</sub>O.
4. When using the <abbr> element, what attribute must be added to provide the full expansion of the term?
    * An abbreviation title must be added so that a user can hover on the abbreviation and see the full version of what the abbreviation represents.

### How CSS Is Structured

1. What are ways we can apply CSS to our HTML?
    * External stylesheet (considered best practice)
    * Internal stylesheet (can be useful in limited circumstances)
    * Inline (discouraged)
2. Why should we avoid using inline styles?
    * Least efficent for maintenance -- would have to run around a website(s) to make changes versus in a single CSS style sheet -- almost unimaginably complex for a bigger project.
    * Mix CSS presentational code with HTML and content - opposite of best practice of keeping content and code separate. 
3. Review the block of code below and answer the following questions:
    * What is representing the selector?
      * h2
    * Which components are the CSS declarations?
      * color: black;
      * padding: 5px;
    * Which components are considered properties?
      * color 
      * padding

### JavaScript Basics

1. What data type is a sequence of text enclosed in single quote marks?
    * String
2. List 4 types of JavaScript operators.
    * Assignment ( = ): assigns values to variables
    * Strict equality ( === ): checks if 2 values are equals, incl. whether of same type of not
    * Addition ( + ): adds two numbers together; also used with strings in concatentation
    * Not, does not equal ( !, !== ): basically inverts/negates what comes to the right of it, so !== means that two values are NOT equal
3. Describe a real world Problem you could solve with a Function.
    * Practical real world website example given in reading is the alert() function, which makes a pop-up box appear in the browser 
    * Generally, the use cases for functions are as widespread as imaginable, as they're reusable blocks of code

### JavaScript Conditionals

1. An if statement checks a [<u>condition</u>] and if it evaluates to [<u>true</u>], then the code block will execute.
2. What is the use of an else if?
    *  It is a way to chain on extra choices / outcomes to the if-else construction, effectively allowing to extend the if statement to multiple conditions 
3. List 3 different types of comparison operators.
    * === and !== — test if one value is identical to, or not identical to, another.
    * < and > — test if one value is less than or greater than another.
    * <= and >= — test if one value is less than or equal to, or greater than or equal to, another.
4. What is the difference between the logical operator && and \|\|?
    * && equals and
    * \|\| equals or

## Things I want to know more about
* Key area to understand better is interacting with the BOM
* Understanding how commonly switch statements and ternary operators are used in professional environments

