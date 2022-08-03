## Class-07 Reading Notes  
<p>My understanding is that working with data is the real key skill set a developer can have in today's world, and objects are absolutely central to that skill set.</p>

### Domain Modeling

1. Explain why we need domain modeling.
    * Domain modeling is the process of creating a conceptual model in code for a specific problem.
    * A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders.
    * As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

### HTML Table Basics

1. Why should tables not be used for page layouts?
    * Layout tables reduce accessibility for visually impaired users:  Because tables are not the right tool for layout, and the markup is more complex than with CSS layout techniques, the screenreaders' output will be confusing to their users.
    * Tables produce tag soup: table layouts generally involve more complex markup structures than proper layout techniques. This can result in the code being harder to write, maintain, and debug.
    * Tables are not automatically responsive: tables are sized according to their content by default, so extra measures are needed to get table layout styling to effectively work across a variety of devices.
2. List and describe 3 different semantic HTML elements used in an HTML <table\>.
    * <table\> tags that enclose the table.
    * <th\> tags that enclose headers, setting out the columns.
    * <tr\> tags that enclose rows.
    * <td\> tags that enclose cells.

### Introducing Constructors

1. What is a constructor and what are some advantages to using it?
    * A type of function that creates an object when invoked.
    * It is much more efficient than object literals when creating many objects with the same basic properties.
2. How does the term this differ when used in an object literal versus when used in a constructor?
    * In an object literal, this refers to an object which is overtly assigned and returned within the function; in a constructor, this refers to an object whose construction and return is effectively automated under the hood.

### Object Prototypes Using A Constructor

1. Explain prototypes and inheritance via an analogy from your previous work experience.
NOTE: This is a very common front end developer interview question
    * In the investment space, I would equate prototypes with template legal documents like term sheets, and inheritance being the process where a new term sheet inherits the previous template when it is created.

## Things I want to know more about

1. The 'heavy' topics from above for me are constructors and prototypes -- I realize that I need to understand these well, and many things yet to come will be built upon these fundamental concepts.