
# Class-34 -- API Integration

This is a relevant topic for pretty much anything in the modern world of web apps.

## [Review API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/)

1. Explain the different between a query string parameter and a path parameter.
    * The path parameter defines the resource location, while the query parameter defines sort, pagination, or filter operations. The user's input (the query) is passed as a variable in the query parameter, while each path parameter must be substituted with an actual value when the client makes an API call.
2. What would our API URL with a path id parameter be given the following information:
    1. Domain: <http://our-site.com>
    2. v3
    3. model name: stuff
    4. id: things
    5. URL would be: <http://our-site.com/v3/stuff/things>
3. We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.
    * Similar to the way you can type into the search field on Google and Google brings backs loads of relevant (or perhaps irrelevant in some cases) information back to you, the user -- so it is with an API interface more generally.

## [Review Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/)

1. Describe how you would use middleware to implement basic and bearer auth.
    * The Basic Authentication processes is initiated by invoking a POST on your /oauth route with a Basic Authorization header.
        * The Basic Auth Middleware should at this point validate the user account in our database, and return an object with a re-authentication/bearer token and the user object or an error object.
    * Bearer Auth
        * First, the tokenAuthentication middleware will re-authenticate the user.
        * If the token is valid (the user is good), the route handler will execute as it normally would.
        * If the token is invalid, or the capability is not present for the user, the system should respond with a standard error.
2. Describe the handshake necessary to implement OAuth.
    * [Google handshake description](https://medium.com/@valeriechapple/how-to-truly-understand-oauth-2-0-69dd3e7574c6#:~:text=The%20OAuth%202.0%20handshake%20involves,finally%20access%20the%20user's%20information.)
        * An app registers with Google, obtaining a client_id and a client_secret.
        * An app provides a way for a user to signal they wish to sign in to Google.
        * The app redirects the user to a Google URL to sign in, attaching the app's credentials and a random state variable, as well as other specifications, to the URL query string.
        * The user chooses to sign in and grant permissions to the app.
        * After the user grants permission, Google sends a response to the app at an agreed upon route (a callback route). The response contains an authentication code and the exact same state variable it received.
        * The app checks that the state variable is the same state variable from step 3 before continuing with the OAuth flow.
        * The app uses the authentication code from Google to request an access_token, using a POST request.
        * If the authorization code is valid, Google will respond with an access_token (and possibly arefresh_token). Save these tokens for future use.
        * The access_token is used to access the user’s data without requiring the user to sign in. That is, send the access_token in the Authorization header (such as a Bearer asdsadfhsdiwej191293djsd) to one of Google’s API endpoints. For example, an endpoint to get basic user information is <https://www.googleapis.com/auth/userinfo.email>. This step can be repeated for as long as the access_token is valid. Next step is to consider looking at the Google API Documentation on refresh_token.
3. Describe how Role Based Access Control works to a non-technical friend.
    * In a family setting at home, parents have access 'rights' to their own bedroom as well as access to the rooms of their children, but the children only have access rights to their own bedroom -- this is effectively assigning access to a resource based on a user's role.  

## Reflection

1. What are your learning goals after reading and reviewing the class README?
    * Describe and Define
        * Role based access control.
        * Cookies.
        * Fetch and Superagent Authorization Headers.
    * Execute
        * Connect a react application to a deployed API.
        * Login and Authorization using both “Basic Authorization” and a “Bearer Token” with a live server.


## Things I want to know more about

1. Good review on things we have already covered, but a complex topic I have barely scratched the surface of, so plenty more to dig into.
