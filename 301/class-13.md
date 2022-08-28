## Class-13 Reading Notes
<p>This is self-evidently relevant material, as it pertains to how CRUD maps to REST APIs.</p>

### CRUD Basics

1. Which HTTP method would you use to update a record through an API?
    * PUT.
2. Which REST methods require an ID parameter?
    * PUT and DELETE.

### Speed Coding: Building a CRUD API (Watch a Twitch streamer code an Express API in 20 minutes!)

1. What’s the relationship between REST and CRUD?
    * Create, Read, Update, and Delete — CRUD — are the four major functions for interacting with database applications. CRUD functions often play a role in web-based REST APIs, where they map (albeit poorly) to the HTTP methods GET, POST, DELETE, PUT, and PATCH. Importantly, REST APIs can still expose functionality not corresponding to CRUD, so long as they use the appropriate HTTP method. [Source](https://nordicapis.com/crud-vs-rest-whats-the-difference/)
2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?
    * Identify Object Model
    * Create Model URIs
    * Determine Representations
    * Assign HTTP Methods
    * More Actions (e.g. logging, security, etc.)

## Things I want to know more about

1. I look forward to actually implementing some of this during labs this week -- from the implementation will spring many questions, I'm sure.
