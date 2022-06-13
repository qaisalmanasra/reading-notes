# **Bearer Authorization**
### ***What is JSON Web Token?***
#### JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

### ***When should you use JSON Web Tokens?***
#### Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

#### Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

### ***Summury***

#### JWT is a very modern, simple and secure approach which extends for Json Web Tokens. Json Web Tokens are a stateless solution for authentication. So there is no need to store any session state on the server, which of course is perfect for restful APIs. Restful APIs should always be stateless, and the most widely used alternative to authentication with JWTs is to just store the user's log-in state on the server using sessions. But then of course does not follow the principle that says that restful APIs should be stateless and that's why solutions like JWT became popular and effective.

#### So now let's know how authentication actually works with Json Web Tokens. Assuming we already have a registered user in our database. So the user's client starts by making a post request with the username and the password, the application then checks if the user exists and if the password is correct, then the application will generate a unique Json Web Token for only that user.

#### The token is created using a secret string that is stored on a server. Next, the server then sends that JWT back to the client which will store it either in a cookie or in local storage.

### **[Reference](https://www.youtube.com/watch?v=926mknSW9Lo)**
### **[Reference](https://jwt.io/introduction/)**
### **[Reference](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)**
### **[Bookmark](https://www.npmjs.com/package/jsonwebtoken)**

