angular-authentication
======================

Angular Authentication
Source: http://www.sitepoint.com/implementing-authentication-angular-applications/


There is a difference in the way user management is implemented in traditional server-driven applications and Single Page Applications. The only way in which an SPA can interact with its server components is through AJAX. This is true even for logging in and logging out.

The server responsible for identifying the user has to expose an authentication endpoint. The SPA will send the credentials entered by the user to this endpoint to for verification. In a typical token based authentication system, the service may respond with an access token or with an object containing the name and role of the logged in user after validating the credentials. The client has to use this access token in all secured API requests made to the server.

As the access token will be used multiple times, it is better to store it on the client side. In Angular, we can store the value in a service or a value as they are singleton objects on the client side. But, if the user refreshes the page, the value in the service or value would be lost. In such case, it is better to store the token using one of the persistence mechanisms offered by the browser; preferably sessionStorage, as it is cleared once the browser is closed.

