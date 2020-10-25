# Reading12: OAuth

### Review, Research, and Discussion

1. Why is authentication important? because it enables organizations to keep their networks secure by permitting only authenticated users (or processes) to access its protected resources, which may include computer systems, networks, databases, websites and other network-based applications or services
2. Why should we be careful about storing a user’s password? To prevent any revel for the passwords in the database
3. What is the difference between hashing and encryption? Encryption is a two-way function; what is encrypted can be decrypted with the proper key. Hashing, however, is a one-way function that scrambles plain text to produce a unique message digest.
4. What is the difference between encryption and encoding? Encoding is for maintaining data usability and can be reversed by employing the same algorithm that encoded the content, i.e. no key is used. Encryption is for maintaining data confidentiality and requires the use of a key (kept secret) in order to return to plaintext
5. What is a token used for? It acts like an electronic key to access something

### Terms

**authentication**: is the process of verifying the identity of a person or device.
**authorization**: is a security mechanism to determine access levels or user/client privileges related to system resources including files and services
**encryption**: translates data into another form, or code, so that only people with access to a secret key (formally called a decryption key) or password can read it.
**hashing**: is the process of converting a given key into another value. A hash function is used to generate the new value according to a mathematical algorithm.
**session**: get stored on the client as well as a server. A session creates a file in a temporary directory on the server where registered session variables and their values are stored
**cookie**: are only stored on the client-side machine
**token**
**Basic Auth**: is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request
**encoding**: is the process of converting data from one form to another.
**secret**: a key specialized for a user
**cryptography**: is the science of protecting information by transforming it into a secure format.

### Preview

#### OAuth

OAuth is an open standard for access delegation, commonly used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords.[1] This mechanism is used by companies such as Amazon,[2] Google, Facebook, Microsoft and Twitter to permit the users to share information about their accounts with third party applications or websites.

Generally, OAuth provides clients a "secure delegated access" to server resources on behalf of a resource owner. It specifies a process for resource owners to authorize third-party access to their server resources without sharing their credentials. Designed specifically to work with Hypertext Transfer Protocol (HTTP), OAuth essentially allows access tokens to be issued to third-party clients by an authorization server, with the approval of the resource owner. The third party then uses the access token to access the protected resources hosted by the resource server.[3]

OAuth is a service that is complementary to and distinct from OpenID. OAuth is unrelated to OATH, which is a reference architecture for authentication, not a standard for authorization. However, OAuth is directly related to OpenID Connect (OIDC), since OIDC is an authentication layer built on top of OAuth 2.0. OAuth is also unrelated to XACML, which is an authorization policy standard. OAuth can be used in conjunction with XACML, where OAuth is used for ownership consent and access delegation whereas XACML is used to define the authorization policies (e.g., managers can view documents in their region).
