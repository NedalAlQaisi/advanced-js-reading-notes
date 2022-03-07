# Bearer Authorization

## What's JWT?
`JWT` or `JSON Web Token`, is an open standard used to share security information between two parties — a `client` and a server. Each JWT contains encoded JSON objects, including a set of claims. JWTs are signed using a cryptographic algorithm to ensure that the claims cannot be altered after the token is issued.


## What's JSON?
For beginning developers, `JSON` stands for `JavaScript Object Notation` and is a text-based format for transmitting data across web applications. It stores information in an easy-to-access manner, both for developers and computers. It can be used as a data format by any programming language and is quickly becoming the preferred syntax for APIs, surpassing XML.


## What Are Tokens?
A token is a string of data that represents something else, such as an identity. In the case of `authentication`, a non-JWT based token is a string of characters that allow the receiver to validate the sender’s identity. The important distinction here is lack of meaning within the characters themselves. 

## How JWT works?
JWTs differ from other web tokens in that they contain a set of claims. Claims are used to transmit information between two parties. What these claims are depends on the use case at hand. For example, a claim may assert who issued the token, how long it is valid for, or what permissions the `client` has been granted.

A `JWT` is a string made up of three parts, separated by dots (.), and serialized using base64. In the most common serialization format, compact serialization, the `JWT` looks something like this: 
```
xxxxx.yyyyy.zzzzz.
```
Once decoded, we will get two JSON strings:

1. The header and the payload.
2. The signature. 

The JOSE (JSON Object Signing and Encryption) header contains the type of token — JWT in this case — and the signing algorithm.  

The payload contains the claims. This is displayed as a JSON string, usually containing no more than a dozen fields to keep the `JWT` compact. This information is typically used by the server to verify that the user has permission to perform the action they are requesting.

There are no mandatory claims for a `JWT`, but overlaying standards may make claims mandatory. For example, when using `JWT` as bearer `access token` under OAuth2.0, iss, sub, aud, and exp must be present. some are more common than others. 

The signature ensures that the token hasn’t been altered. The party that creates the `JWT` signs the header and payload with a `secret` that is known to both the issuer and receiver, or with a private key known only to the sender. When the token is used, the receiving party verifies that the header and payload match the signature. 

## Why Use JWT?
In short, JWTs are used as a secure way to authenticate users and share information.

Typically, a private key, or `secret`, is used by the issuer to sign the JWT. The receiver of the JWT will verify the signature to ensure that the token hasn’t been altered after it was signed by the issuer. It is difficult for unauthenticated sources to guess the signing key and attempt to change the claims within the JWT.

Not all signing algorithms are created equal though. For example, some signing algorithms use a `secret` value that is shared between the issuer and the party that verifies the JWT. Other algorithms use a public and private key. The private key is known only to the issuer, while the public key can be widely distributed. The public key can be used to verify the signature, but only the private key can be used to create the signature. This is more secure than a shared `secret` because the private key only needs to exist in one place.

Because of this, the server does not need to keep a database with the information needed to identify the user. For developers, this is great news — the server that issues the JWT and the server that validates it do not have to be the same. 

# Discussion


#### What can we do with an authorization code?

An authorization code is an alphanumeric password that authorizes its user to purchase, sell or transfer items, or to enter information into a security-protected space.

#### What can we do with an access token?

Access tokens are the thing that applications use to make `api` requests on behalf of a user. The `access token` represents the authorization of a specific application to access specific parts of a user’s data.

#### What’s a benefit of using OAuth instead of our basic authentication?

It enables apps to obtain limited access (scopes) to a user’s data without giving away a user’s password. It decouples `authentication` from authorization and supports multiple use cases addressing different device capabilities. It supports server-to-server apps, browser-based apps, mobile/native apps, and consoles/TVs.


### [Back to the HOME](./README.md)