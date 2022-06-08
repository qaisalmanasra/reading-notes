# **Authentication**
## ***Securing Passwords***
#### Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, designed to calculate a digest of huge amounts of data in as short a time as possible. Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.
#### The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords.
## ***PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM***
#### Brute Force attack: Hashes can't be reversed, so instead of reversing the hash of the password, an attacker can simply keep trying different inputs until he does not find the right now that generates the same hash value, called brute force attack.
#### Hash Collision attack: Hash functions have infinite input length and a predefined output length, so there is inevitably going to be the possibility of two different inputs that produce the same output hash. MD5, SHA1, SHA2 are vulnerable to Hash Collision Attack i.e. two input strings of a hash function that produce the same hash result.
## ***BCrypt, IT's SLOW AND STRONG AS HELL***
#### To overcome such issues, we need algorithms which can make the brute force attacks slower and minimize the impact. Such algorithms are PBKDF2 and BCrypt, both of these algorithms use a technique called Key Stretching.
#### Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.
## ***Basic access authentication***
#### In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>,
### `Features`
#### HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.
### `Security`
#### The BA mechanism does not provide confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit and not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.
### `Protocol`
> * Server side
#### When the server wants the user agent to authenticate itself towards the server after receiving an unauthenticated request, it must send a response with a HTTP 401 Unauthorized status line[7] and a WWW-Authenticate header field.[8]

The WWW-Authenticate header field for basic authentication is constructed as following:

WWW-Authenticate: Basic realm="User Visible Realm"

The server may choose to include the charset parameter from RFC 7617:[3]

WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"

This parameter indicates that the server expects the client to use UTF-8 for encoding username and password (see below).
>* Client side
#### When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.

#### The Authorization header field is constructed as follows:

- The username and password are combined with a single colon (:). This means that the username itself cannot contain a colon.
- The resulting string is encoded into an octet sequence. The character set to use for this encoding is by default unspecified, as long as it is compatible with US-ASCII, but the server may suggest use of UTF-8 by sending the charset parameter.
- The resulting string is encoded using a variant of Base64 (+/ and with padding).
- The authorization method and a space (e.g. "Basic ") is then prepended to the encoded string.
### **[Reference](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)**
### **[Reference](https://en.wikipedia.org/wiki/Basic_access_authentication)**
### **[Reference](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)**
### **[Reference](https://www.npmjs.com/package/bcrypt)**