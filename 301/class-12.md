## Class-12 Reading Notes  
<p>This is self-evidently relevant material, as it pertains to REST, Mongo, Node.js, Express, etc.</p>

### Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:
    * 100’s = informational codes -- usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client.
    * 200’s = generally speaking, these are success codes.
    * 300’s = redirection, i.e. the resource the client requested isn't available, and the client is redirected to a new location, and must issue a new request for that new location.
    * 400’s = error codes, like the famous 404 -- invalid requests (for various reasons: timeouts, wrong URI, missing authentication, etc.) a client sent to a server.
    * 500’s = server error codes -- various reasons, incl. overwhelmed servers or unreachable servers behind proxies, but can also be related to client requests that trigger error exceptions on the server; these errors can be temporary or permanent, and best for the client to retry the same request.
2. What is a status code 202? 
    * Accepted:  
        * Often used for asynchronous processing.
        * This code tells the client that the request was valid, but its processing will finish sometime in the future. 
        * The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.
3. What is a status code 308?
    * Permanent redirect:
        * This tells the client to use another URL to access the resource and not use the current URL anymore. 
        * It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.
4. What code would you use if an update didn’t return data to a client?
    * 204 No Content - A proper code for updates that don’t return data to the client, for example when just saving a currently edited document.
5. What code would you use if a resource used to exist but no longer does?
    * 410 Gone - This is like 404 but we know that the resource existed in the past, but it got deleted or somehow moved, and we don’t know where.
6. What is the ‘Forbidden’ status code?
    * 403: The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.

### Build A REST API With Node.js, Express, & MongoDB - Quick

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
    * When you deploy, you do not want to share your local host.
2. What is middleware?
    * Code that runs when the server gets a request but before it gets passed to the routes.
3. What does app.use(express.json()) do?
    * Allows the server to accept JSON as a body instead of as a POST or GET element, etc.
4. What does the /:id mean in a route?
    * It means that it is a parameter that can be accessed by typing in request.params.id -- this gives access to whatever is passed in before the first slash.
5. What is the difference between PUT and PATCH?
    * PATCH allows you to only update on what the user passes (e.g. a subscriber passing in their name); PUT updates all the information (i.e. all the information about the aforementioned subscriber), instead of just the information that is passed.
6. How do you make a default value in a schema?
    * E.g. for subscribeDate:
        * default: Date.now
7. What does a 500 error status code mean?
    * Error on server, i.e. nothing to do with user or API -- entire issue is with server.
8. What is the difference between a status 200 and a status 201?
    * 200: a success message that relays that the request was received and understood and is being processed.
    * 201: a success message that indicates that a request was successful and as a result, a resource has been created (e.g. a new page).

## Things I want to know more about

1. I look forward to actually implementing some of this during labs this week -- from the implementation will spring many questions, I'm sure.
