# Reading11: Authentication

## Review, Research, and Discussion

1. Explain what a “Singleton” is (in Computer Science terms)
   it is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes
3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

## Terms

**Router Middleware** : functions that have access to the request object, the response object.
**Dynamic Module Loading** :import/export aim to provide a backbone for the code structure. That’s a good thing, as code structure can be analyzed, modules can be gathered and bundled into one file by special tools.
**Singleton Pattern** :design pattern that restricts the instantiation of a class to one “single” instance.
**CRUD -> REST Method Matches** CRUD: CREATE READ UPDATE DELETE -> REST: GET POST PUT DELETE
**Mock Testing** : an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules.

## Preview

##### Authorization

This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

##### Authentication

basic access authentication is a method for an HTTP client to provide a user name and password when making a request. it does not require cookies, session identifiers, or login pages.

##### BCrypt

bcrypt is a password-hashing function. Besides incorporating a salt to protect against rainbow table attacks, bcrypt is an adaptive function: over time, the iteration count can be increased to make it slower, so it remains resistant to brute-force search attacks even with increasing computation power.

##### JSON Web Tokens (JWT)

JSON Web Token (JWT) is a compact, URL-safe means of representing claims to be transferred between two parties,The claims in a JWT are encoded as a JSON object that is used as the payload of a JSON Web Signature (JWS) structure or as the plaintext of a JSON Web Encryption (JWE) structure.

##### JWT structure

JSON Web Tokens consist of three parts separated by dots (.), which are:

Header : The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used.

Payload : payload contains the claims. Claims are statements about an entity (typically, the user) and additional data.

Signature : To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.
