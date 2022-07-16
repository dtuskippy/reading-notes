## Class-06 Reading Notes  
<p>My understanding is that working with data is the real key skill set a developer can have in today's world, and objects are absolutely central to that skill set.</p>

### JavaScript Object Basics

1. How would you describe an object to a non-technical friend you grew up with?
    * It's main purpose is to group data, usually repeatable identical data types together into an aggregated unit, e.g. everybody has a driver's license with the same basic data *properties* on it, like name, date of birth, and license number -- but of course the *values* for individuals are all different -- effectively, driver's license data is an object
2. What are some advantages to creating object literals?
    * Sending a single object (series of structured, related data items) is much more efficient than sending items individually -- benefits of consolidation
3. How do objects differ from arrays?
    * When you want to identify individual items by name, objects are easier than arrays to work with
4. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.
    * I wasn't happy with the MDN writing, but found this information [here](https://www.samanthaming.com/tidbits/65-dot-vs-bracket-notation/) online, which states the following:
        * *Both notations can access object properties -- From Airbnb's style guide:* ***Always use Dot. And when you want to access object property with a variable, use Bracket.***
5. Evaluate the code below. What does the term this refer to and what is the advantage to using this?
    * this keyword refers to the current object the code is being written inside

### Introduction to the BOM

1. What is the DOM?
    * The data representation of the objects that comprise the structure and content of a document on the web.
    * Programming interface for web documents -- it represents the page so that programs can change the document structure, style, and content.

2. Briefly describe the relationship between the DOM and JavaScript.
    * The DOM is not part of the JavaScript language, but is instead a Web API used to build websites.
    * Without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, SVG documents, and their component parts.


## Things I want to know more about

1. I have only had brief exposure to the DOM, so really need to work to understand it.