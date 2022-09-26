# Class-07 Reading Notes

It's pretty self-evident that security is extremely relevant to the design, development and deployment of web apps.

## [Intro to JWT](https://jwt.io/introduction/)

1. What is a JSON Web Token (JWT)?
    * JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. 
    * This information can be verified and trusted because it is digitally signed. 
    * JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
2. When should we use JSON Web Tokens?
    * Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.
    * Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.
3. Claims are expected in which structural component of a JWT?
    * In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:
      * Header
      * Payload
      * Signature
    * The second part of the token is the payload, which contains the claims.
      * Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.

## [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

1. If I get a JWT and I can decode the payload, how can we call that secure?
    * If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore.
2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
    * The hashed content and secret.
3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.
    * The sender and receiver encrypt the message essentially with a key, so even if somebody intercepts the message, they would need the key to effectively change the message and resend it.

## [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

1. Why use JWT?
    * This information can be verified and trusted because it is digitally signed.
2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
    * [Compact](https://www.linkedin.com/pulse/demystifying-json-web-token-jwt-sanchit-khurana/): The size is so compact that tokens can be transferred easily and fastly through URL, POST parameter, or inside an HTTP header, i.e. this lack of size means it does not slow down the system.
    * Self-contained: They contain all the relevant information of the user and it doesn't need to query it again, i.e. 'one-stop shopping'.
3. What are the three components (the structure) of a JWT signature?
    * Header
    * Payload
    * Signature


## Bookmarks

1. [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)


## Things I want to know more about

1. Web security is a pretty complex realm, and would be good to learn how to navigate that world and understand what best practices are.