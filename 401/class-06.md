# Class-06 Reading Notes

It's pretty self-evident that security is extremely relevant to the design, development and deployment of web apps.

## [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

1. Explain to a non-technical friend how you would safely hash and store a password.
    * Hashing turns your password (or any other piece of data) into a short string of letters and/or numbers using an encryption algorithm. If a website is hacked, cyber criminals don't get access to your password. Instead, they just get access to the encrypted “hash” created by your password.
    * How hashing works in practice:
        * Step 1 – A user visits a site and fills in a form to create their username and password.
        * Step 2 – That password is put through a hash function and the hash is stored in the database.
        * Step 3 – When a user logs in they enter their password again on the site.
        * Step 4 – That entered password is run through the same hashing function as was used before.
        * Step 5 – The server checks this hash against the one stored for the user in the database.
        * Step 6 – If the two hashes match exactly, the user is granted access.
    * The friend should use a password manager (personally use LastPass): a [password manager](https://www.cnet.com/tech/services-and-software/best-password-manager/) is essentially an encrypted digital vault that stores secure password login information you use to access apps and accounts on your mobile device, websites and other services. In addition to keeping your identity, credentials and sensitive data safe, the best password managers also have a password generator to create strong, unique passwords and ensure you aren't using the same password in multiple places.
2. What is Bcrypt?
    * Like the PBKDF2 algorithm, BCrypt uses a technique called Key Stretching.
        * [Key stretching](https://en.wikipedia.org/wiki/Key_stretching) techniques are used to make a possibly weak key, typically a password or passphrase, more secure against a brute-force attack by increasing the resources (time and possibly space) it takes to test each possible key.
    * BCrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.
3. Why might you use something like Bcrypt?
    * Bycrpt has a work factor value that determines how slow the hash function will be, i.e. a different work factor will generate different hash values in different time spans, which makes it extremely resistant to brute force attacks. W
    * When computers become faster next year the work factor can be increased to balance it out i.e. to make the attack slower.

## [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

1. What is Basic Authentication?
    * In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request.
2. What properties are necessary in the header of a Basic Auth request?
    * In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :.
3. How are username:password in Basic Auth encoded?
    * The BA mechanism does not provide confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit and not encrypted or hashed in any way.
    * Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.

## [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

1. Define the authentication process to a non-technical recruiter.
    * Authentication is the process of verifying that an individual, entity or website is whom it claims to be.
    * Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.
2. How should your error messaging respond (both HTTP and HTML)? Why?
    * Incorrectly implemented error messages in the case of authentication functionality can be used for the purposes of user ID and password enumeration.
    * An application should respond (both HTTP and HTML) in a generic manner.
3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.


## Things I want to know more about

1. Web security is a pretty complex realm, and would be good to learn how to navigate that world and understand what best practices are.