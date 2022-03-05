# Authentication

## Definition of Authentication

Definition: Authentication is the process of recognizing a user’s identity. It is the mechanism of associating an incoming request with a set of identifying credentials. The credentials provided are compared to those on a file in a database of the authorized user’s information on a local operating system or within an authentication server.

Description: The authentication process always runs at the start of the application, before the permission and throttling checks occur, and before any other code is allowed to proceed. Different systems may require different types of credentials to ascertain a user’s identity. The credential often takes the form of a password, which is a secret and known only to the individual and the system. Three categories in which someone may be authenticated are: something the user knows, something the user is, and something the user has.

## HTTP basic Authentication

HTTP basic authentication is a simple challenge and response mechanism with which a server can request authentication information (a user ID and password) from a client. The client passes the authentication information to the server in an Authorization header. The authentication information is in base-64 encoding.

The HTTP basic authentication scheme can be considered secure only when the connection between the web client and the server is secure. If the connection is insecure, the scheme does not provide sufficient security to prevent unauthorized users from discovering the authentication information for a server. If we think that a password might be intercepted, use basic authentication with SSL encryption to protect the user ID and password.

If a client makes a request for which the server expects authentication information, the server sends an HTTP response with a 401 status code, a reason phrase indicating an authentication error, and a WWW-Authenticate header. Most web clients handle this response by requesting a user ID and password from the user.


## Securing Passwords with Bcrypt Hashing Function

The `BCrypt Hashing` function allows us to build a password security platform that scales with computation power and always hashes every password with a salt.

### Who uses bcrypt and why?
Bcrypt is a password hashing algorithm and it is not the same as just encryption in general. It is used specifically encrypting and securely storing passwords. It is used primarily when a user enters a password and that password needs to be stored in a database in a way that the original password could not be guessed even if the system was attacked and the database got compromised.

### Comparisons to other hashes
#### Comparison to md5
Md5 is not suitable to encrypt sensitive information. It can be and has been cracked. It is also a fast hash like the SHA algorithms, but with the additional problem of being directly crackable.

#### Comparison to sha, sha256, sha512
The sha algorithms are fast hashes and there is no concept of salt. Both of these make them a bad choice for passwords hashing. Password hashing algorithms must be slow and use salt to discourage rainbow table attacks.

### Generate a salt and hash on separate function calls.
```
// app.js
const bcrypt = require("bcrypt");
const saltRounds = 8;
const plainTextPassword1 = "nedal";
bcrypt
  .genSalt(saltRounds)
  .then(salt => {
    console.log(`Salt: ${salt}`);
    return bcrypt.hash(plainTextPassword1, salt);
  })
  .then(hash => {
    console.log(`Hash: ${hash}`);
    // Store hash in your password DB.
  })
  .catch(err => console.error(err.message));

```
Using the "Promise" pattern to control the asynchronous nature of JavaScript, in this technique, we first create a salt through the `bcrypt.genSalt` function that takes the cost, `saltRounds`. Upon success, we get a `salt` value that we then pass to `bcrypt.hash` along with the password, `plainTextPassword1`, that we want to hash. The success of `bcrypt.hash` provides us with the hash that we need to store in our database. In a full implementation, we would also want to store a username along with the hash in this final step.

In the first run, I got the following results in the command line:
```
Salt: $2a$08$Pi/kB1fIItJd/nKa.
Hash: $2a$08$Pi/kB1fIItJd/nKa.dbM6eymQl2sVLHAsGy98lJ6Y9vz7m62cGuq2
```
#### NOT: The `Promise` pattern
The `Promise` object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.
## 
## 
## 

### [Back to the HOME](./README.md)