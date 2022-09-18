# Class-04 Reading Notes

I have some familiarity with the differences between sql and no sql from my business background, but look forward to digging deeper.

## nosql vs sql

1. What type of database is the best fit for the complex query intensive environment?
    * SQL databases are a good fit for a complex query intensive environment whereas NoSQL databases are not a good fit for complex queries.
    * At a high-level, NoSQL doesn't have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
2. What type of database is the best fit for hierarchical data storage?
    * NoSQL is a better fit for hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data; NoSQL databases are highly preferred for large data sets (i.e for big data).
3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
    * SQL is vertically scalable, i.e. you must increase the capacity of the actual server the software is running on, whereas NoSQL is horizontally scalable, meaning you can more easily spread the software (shard) across many different servers -- the fact that vertically scalable is clearly more limited than horizontally scalable, NoSQL is the more scalable solution overall.

## sql modeling techniques

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
    * E.g. one-to-many would be department with many employees attached to that department.  
    * A single record from one table can be linked to zero or more rows in another table.
2. Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.
    * Create a diagram.
3. Explain the difference between a primary and foreign key.
    * Primary keys uniquely identify each row in a table.  (A table typically has one primary key, but can have more.  When the key has more than one column, it is called a compound key).
    * Foreign key is a column or set of columns which match a primary key in another table.

## nosql vs sql (video)

1. How do we treat keywords and parameters differently in SQL syntax?
    * Parameters are used to exchange data between stored procedures and functions and the application or tool that called the stored procedure or function.
    * Keywords are words that have significance in SQL -- certain keywords, such as SELECT, DELETE, or BIGINT, are reserved and require special treatment for use as identifiers such as table and column names.
2. Define normalization within the context of schemas and data.
    * Normalization is the process of creating a maximally efficient relational database -- essentially, databases should be organized to decrease redundancy and avoid dependence anomalies.
    * Also for the sake of users, your database structure should make intuitive sense.
3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
    * In a one-to-one relationship, one record of the first table will be linked to zero or one record of another table. E.g. each employee in the Employee table will have a corresponding row in EmployeeDetails table that stores the current passport details for that particular employee.
    * In a one-to-many relationship, e.g a sales department has 1K employees, so the single sales department ID# has a relationship with 1K employee ID# records in the database.
    * In a many-to-many relationship, e.g. the company has thousands of software developers with associated employee ID# with approximately 80% of the developers matching up to a *skills ID#* record for SQL.

## Things I want to know more about

1. We obviously had some limited experience with NoSQL via Mongo in 301, so I look forward to digging into SQL in 401.