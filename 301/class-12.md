## Class-14 Reading Notes  
<p>This is relevant to me personally from a slightly different angle -- I'm based in Europe, and the percentage of women who are startup founders or venture capitalists is incredibly small.</p>

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
2. What is middleware?
3. What does app.use(express.json()) do?
4. What does the /:id mean in a route?
5. What is the difference between PUT and PATCH?
6. How do you make a default value in a schema?
7. What does a 500 error status code mean?
8. What is the difference between a status 200 and a status 201?

## Things I want to know more about

1. I am curious about the topic from a startup perspective -- female founders are extremely rare in Europe where I'm based, and it is sometimes striking when you see that different market view brought to the table -- there is clearly an untapped market opportunity out there.
