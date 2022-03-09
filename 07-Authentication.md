# Access Control (ACL)

## Discussion

### When is Basic Authorization used vs. Bearer Authorization?

- Basic Authentication is a method for an HTTP user agent (Web Browser) to provide a username and password when making a request.
- Bearer tokens are a much simpler way of making API requests, since they don't require cryptographic signing of each request. The tradeoff is that all API requests must be made over an HTTPS connection, since the request contains a plaintext token that could be used by anyone if it were intercepted.

### What does the JSON Web Token package do?

- To share security information between two parties  a `client` and a `server`. Each JWT contains encoded JSON objects, including a set of claims. JWTs are signed using a cryptographic algorithm to ensure that the claims cannot be altered after the token is issued.

### What considerations should we make when creating and storing a SECRET?

1. Differentiate Between Secrets and Identifiers
2. Establish a Circle of Trust
3. Gain Visibility into the Chain of Trust
4. Encrypt Data Using a KMS
5. Rotate Secrets Frequently
6. Automate Password Creation
7. Store Secrets Responsibly
8. Detect Unauthorized Access

___

## Term

Term | Definition
------------ | ------------
Encryption | Encryption attempts to make information unreadable by anyone who is not explicitly authorized to view that data. People or devices can be authorized to access encrypted data in many ways, but typically this access is granted via passwords or decryption keys.
Token |  Token is a tiny piece of code that contains a large amount of data. Information about the user, permissions, groups, and timeframes is embedded within one token that passes from a server to a user's device. Plenty of websites use access tokens.
Bearer |  is an HTTP authentication scheme that involves security tokens called bearer tokens. The name `Bearer authentication` can be understood as give access to the bearer of this token.
Secret | These non-human privileged credentials are often called “secrets” and refer to a private piece of information that acts as a key to unlock protected resources or sensitive information in tools, applications, containers, DevOps and cloud-native environments.
JWT | `JWT` or `JSON Web Token`, is an open standard used to share security information between two parties a `client` and a `server`. Each JWT contains encoded JSON objects, including a set of claims. JWTs are signed using a cryptographic algorithm to ensure that the claims cannot be altered after the token is issued.

___

# Types of Access Control (ACL)

- `Role Based Access Control (RBAC)`
- Attribute Based Access Control (ABAC)
- Discretionary access control (DAC)
- Mandatory access control (MAC)

# RBAC

## Definition

Access control based on user roles (a collection of access authorizations a user receives based on an explicit or implicit assumption of a given role). Role permissions may be inherited through a role hierarchy and typically reflect the permissions needed to perform defined functions within an organization. A given role may apply to a single individual or to several individuals.

## Some of the designations in an RBAC tool can include

- Management role scope ==> it limits what objects the role group is allowed to manage.
- Management role group ==> you can add and remove members.
- Management role ==> these are the types of tasks that can be performed by a specific role group.
- Management role assignment ==> this links a role to a role group.

## Benefits of RBAC

- Reducing administrative work and IT support.
- Maximizing operational efficiency.
- Improving compliance.

## Types of access control

Discretionary access control (DAC)
Mandatory access control (MAC)
Role Based Access Control (RBAC)
Attribute Based Access Control (ABAC)

### [Back to the HOME](./README.md)
