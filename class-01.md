## Class-01 Reading Notes  
### Getting Started

1. Compose a short poem describing how HTTP sends data between computers.
    * HTTP like a bow in the quiver
    * From A to B it's fixing to deliver
    * From north to south and from shore to shore
    * Here's hoping you don't wind up with a 404
2. Describe how HTML, CSS, and JS files are “parsed” in the browser.
    * First, the browser parses the HTML, and as part of the process will recogize link or script elements for CSS and JS respectively
    * It will then request CSS or JS files it has found from the server, and subsequently parse them
    * From the parsed HTML, an in-memory DOM tree is generated; from the parsed CSS, and in-memory CSSOM structure is generated; and parsed JS is compiled and executed
    * Eventually a visual representation of the page is painted to the screen for the user to see and interact with
3. How can you find images to add to a Website?
    * An obvious place to start is with [Google Images](https://images.google.com/) -- care must be taken not to violate copyright, and filtering via usage rights for Creative Commons licenses is a good practice
4. How do you create a String vs a Number in JavaScript?
    * Strings are effectively text and enclosed in single or double quotes, as long as the single or double quotes are not mixed
    * Numbers are *just numbers,* and are not enclosed in quotes
5. What is a Variable and why are they important in JavaScript?
    * Variables are containers that contain values, e.g. let day = "Monday";
    * Variables are the key basis that make computer programs dynamic, by allowing values to change

### Introduction to HTML

1. What is an HTML attribute?
    * Attributes contain extra information about an element that doesn't appear in the content itself; examples include links and CSS reference identifiers
2. Describe the Anatomy of an HTML element.
    * Basic anatomy includes opening and closing tags that enclose the content itself, and also attributes which are placed within the opening tag, e.g. <p href="https://www.cityofdavis.org/">Davis, California</p>
3. What is the Difference between <article> and <section> element tags?
    * Article contains independent content that doesn't require other context, e.g. news site article, blog post
    * Section divides a page into different sections like team, location, contact information
4. What Elements does a “typical” website include?
    * header: usually stays same across website; e.g. for a company site, this is where the logo, company name, and company motto would 
    * navigation bar: usually stays same across website, and often in the header; links to other pages on the website
    * main content: format may stay same across website, but this is where the unique content that gives the whole purpose of having separate web pages, e.g. for a company site, pages for products, about us, and contact us would all have unique content in the main portion 
    * sidebar: usually stay same across website; sort of a second header in some cases, with navigation, some ads, etc.
    * footer: usually stays same across website; where detailed, almost administrative information goes, like copyright information or redundant navigation, but also where ads are served, etc.
5. How does metadata influence Search Engine Optimization?
    * it is important to optimize metadata like page titles and meta descriptions for every page; this helps search engines determine what your site's content is about and whether it is relevant to include in search results.
6. How is the <meta> HTML tag used when specifying metadata?
    * It is commonly used to specify site's character set, e.g. UTF-8, and the use of name and content to describe the content itself, the author of the content, viewport information, etc.


### Miscelleneous

1. What is the first step to designing a Website?
    * *Project ideation* -- basically this means actually defining what you hope to accomplish by publishing the website, i.e. defining goals, including various stakeholders, etc.
2. What is the most important question to answer when designing a Website?
    * *What exactly do I want to accomplish?* -- just basically list all the goals of the site
3. Why should you use an <h1> element over a <span> element to display a top level heading?
    * From a content / styling perspective, you can use either an h1 or a span element, but by using the span element, you lose the all-important semantic meaning that the h1 provides
4. What are the benefits of using semantic tags in our HTML?
    * Using semantic tags has all the typical benefits of using any standard that is understood universally, i.e. stick to the standard so that all varieties of human (other developers) and non-human (search engines) actors can interact effectively with your site
5. Describe 2 things that require JavaScript in the Browser?
    * Generally make a website dynamic by using the logic of JS; e.g. storing values in variables, the use of conditional programming to react to user input, etc.
6. How can you add JavaScript to an HTML document?
    * Via the script element, e.g. <script src="app.js"></script>

## Things I want to know more about
* Key area to understand better is interacting with the BOM

