# Class-04 Reading Notes

As we enter the back-end world of web apps, clearly Node.js is a key topic to master for full stack JS apps.

## nosql vs sql

1. What type of database is the best fit for the complex query intensive environment?
    * SQL databases are A good fit for the complex query intensive environment whereas NoSQL databases are not A good fit for complex queries. 
    * On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
2. What type of database is the best fit for hierarchical data storage?
    * NoSQL is a better fit for hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data; NoSQL databases are highly preferred for large data sets (i.e for big data).
3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
    * SQL is vertically scalable, i.e. you must increase the capacity of the actual server the software is running on, whereas NoSQL is horizontally scalable, meaning you can more easily spread the software (shard) across many different servers -- the fact that vertically scalable is clearly more limited than horizontally scalable, NoSQL is the more scalable solution overall.

## sql modeling techniques

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
    * E.g. one-to-many would be department with many employees attached to that department.  A single record from one table can be linked to zero or more rows in another table.
2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
    * Create a diagram.
3. Explain the difference between a primary and foreign key.
    * Primary keys uniquely identify each row in a table.  (A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key).
    * Foreign key is a column or set of columns which match a primary key in another table.

## nosql vs sql (video)

1. How do we treat keywords and parameters differently in SQL syntax?
    * 
2. Define normalization within the context of schemas and data.
    * 
3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
    * 

## Things I want to know more about

1. I would like to dig more into understanding the guts of Chrome's V8 JS Engine.