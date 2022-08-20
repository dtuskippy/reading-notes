## Class-8 Reading Notes  
<p>API design is self-evidently relevant in the world of web services.</p>

### API Design Best Practices

1. What does REST stand for?
    * Representational State Transfer (REST).
2. REST APIs are designed around a ____.
    * REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.
3. What is an identifier of a resource? Give an example.
    * A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:
        * https://adventure-works.com/orders/1
4. What are the most common HTTP verbs?
    * The most common operations are GET, POST, PUT, PATCH, and DELETE.
5. What should the URIs be based on?
    * When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).
6. Give an example of a good URI.
    * https://adventure-works.com/orders // Good example
    * https://adventure-works.com/create-order // Bad example, i.e. Avoid
7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
    * 'Chatty' web apis mean that you the API naming is too granular and the web server is bombarded with too many requests, i.e. it's a bad thing -- KISS principle applies here.
8. What status code does a successful GET request return?
    * 200
9. What status code does an unsuccessful GET request return?
    * 404
10. What status code does a successful POST request return?
    * 201
11. What status code does a successful DELETE request return?
    * 204



## Things I want to know more about

1. I am very interested in actually working with APIs -- I'm not a newbie to the concept, but a newbie in terms of actual implementation.