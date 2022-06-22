## Design Webpages with CSS Reading Notes

### Defining CSS

* Excerpts from [(CSS on Wikipedia)](https://en.wikipedia.org/wiki/CSS): 

  * *Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML or XML (including XML dialects such as SVG, MathML or XHTML). CSS is a cornerstone technology of the World Wide Web, alongside HTML and JavaScript.*
  * *CSS is designed to enable the separation of presentation and content, including layout, colors, and fonts.*

### Basic CSS Overview

* Whereas HTML is used to create the structure and actual content of a web page (such as written text), CSS is responsible for the design or style of the website, including the layout, visual effects and background color.
* CSS uses *selectors* to select items in html to format, e.g.
  * Universal selector: *
  * Type selector: elementname
  * Class selector: .classname
  * ID selector: #idname
  * Attribute selector: [attr=value]
* The most standard way of coding CSS is to do so 'externally', by using a separate stylesheet with a css extension; the *stylesheet.css* is linked to the relevant HTML file
* Example code to change the background color of a footer via an *element selection* 
  * footer { 
      background-color: red; 
    }

### CSS online resource

* For a simple guide to coding in CSS, here is a solid [CSS cheat sheet](https://adam-marsden.co.uk/css-cheat-sheet).
