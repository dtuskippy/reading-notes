## Class-15 Reading Notes  
<p>Authorization and authentication frameworks are a highly relevant topic for any modern deployed web app.</p>

### What is Oauth

1. What is OAuth?
    * OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. 
    * In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.
    * It is also helpful to remember that OAuth is about authorization in particular and not directly about authentication. 
    * Authentication is the process of a user/subject proving its ownership of a presented identity, by providing a password or some other uniquely owned or presented factor. 
    * Authorization is the process of letting a subject access resources after a successful authentication, oftentimes somewhere else. 
    * Many people think that OAuth stands for open authentication, but it’s more helpful to understand it by thinking about it as open AUTHorization.
2. Give an example of what using OAuth would look like.
    * The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. 
    * You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.
3. How does OAuth work? What are the steps that it takes to authenticate the user?
    * Let’s assume a user has already signed into one website or service (OAuth only works using HTTPS). The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens (greatly simplified):
        1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
        2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
        3. The first site gives this token and secret to the initiating user’s client software.
        4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
        5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
        6. The user approves (or their software silently approves) a particular transaction type at the first website.
        7. The user is given an approved access token (notice it’s no longer a request token).
        8. The user gives the approved access token to the first website.
        9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
        10. The second website lets the first website access their site on behalf of the user.
        11. The user sees a successfully completed transaction occurring.
        12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
4. What is OpenID?
    * Whereas OAth is about authorization, OpenID is about authentication -- per a commenter on StackOverflow: "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."
    * In 2014, OpenID Connect was released, which reinvented OpenID as an authentication layer for OAuth. In this space, OpenID has found a niche, and the two technologies now complement each other in many implementations.

### Authorization and Authentication flows

1. What is the difference between authorization and authentication?
    * In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.
    * Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.
2. What is Authorization Code Flow?
    * Because regular web apps are server-side apps where the source code is not publicly exposed, they can use the Authorization Code Flow (defined in OAuth 2.0 RFC 6749, section 4.1), which exchanges an Authorization Code for a token. 
    Your app must be server-side because during this exchange, you must also pass along your application's Client Secret, which must always be kept secure, and you will have to store it in your client.
3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
    * When public clients (e.g., native and single-page applications) request access tokens, some additional security concerns are posed that are not mitigated by the Authorization Code Flow alone. This is because:
        * Native apps
            * Cannot securely store a Client Secret. Decompiling the app will reveal the Client Secret, which is bound to the app and is the same for all users and devices.
            * May make use of a custom URL scheme to capture redirects (e.g., MyApp://) potentially allowing malicious applications to receive an Authorization Code from your Authorization Server.
        * Single-page apps
            * Cannot securely store a Client Secret because their entire source is available to the browser.
    * Given these situations, OAuth 2.0 provides a version of the Authorization Code Flow which makes use of a Proof Key for Code Exchange (PKCE) (defined in OAuth 2.0 RFC 7636).
    * The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code. This way, a malicious attacker can only intercept the Authorization Code, and they cannot exchange it for a token without the Code Verifier.
4. What is Implicit Flow with Form Post?
    * You can use OpenID Connect (OIDC) with many different flows to achieve web sign-in for a traditional web app.
    * In one common flow, you obtain an ID token using authorization code flow performed by the app backend. This method is effective and robust, however, it requires your web app to obtain and manage a secret.
    * You can avoid that burden if all you want to do is implement sign-in and you don’t need to obtain access tokens for invoking APIs.
    * Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. 
    * The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls. With this method, you don’t need to obtain, maintain, use, and protect a secret in your application.
5. What is Client Credentials Flow?
    * With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user. 
    * For this scenario, typical authentication schemes like username + password or social logins don't make sense. 
    * Instead, M2M apps use the Client Credentials Flow (defined in OAuth 2.0 RFC 6749, section 4.4), in which they pass along their Client ID and Client Secret to authenticate themselves and get a token.
6. What is Device Authorization Flow?
    * With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. 
    * This avoids a poor user experience for devices that do not have an easy way to enter text. 
    * To do this, device apps use the Device Authorization Flow (ratified in OAuth 2.0), in which they pass along their Client ID to initiate the authorization process and get a token.
7. What is Resource Owner Password Flow?
    * Though not highly recommended, highly-trusted applications can use the Resource Owner Password Flow (defined in OAuth 2.0 RFC 6749, section 4.3), which requests that users provide credentials (username and password), typically using an interactive form. 
    * Because credentials are sent to the backend and can be stored for future use before being exchanged for an Access Token, it is imperative that the application is absolutely trusted with this information.
    * Even if this condition is met, the Resource Owner Password Flow should only be used when redirect-based flows (like the Authorization Code Flow) cannot be used.



## Things I want to know more about

1. I am both curious and confused about the intricacies of authorization and authentication across the web, and know the tech behind it all is ever changing, so I am looking forward to digging deeper.