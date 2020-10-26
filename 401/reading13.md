# Reading13: Bearer Authorization

### Review, Research, and Discussion

In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

- Write the following steps in the correct order:
  Register your application to get a client_id and client_secret
  Ask the client if they want to sign in via a third party
  Receive authorization code
  Redirect to a third party authentication endpoint
  Make a request to the access token endpoint
  Make a request to a third-party API endpoint
  Receive access token
- What can you do with an authorization code? to exchange it for an access token. The code itself is obtained from the authorization server.
- What can you do with an access token? The access token represents the authorization of a specific application to access specific parts of a user's data.
- What’s a benefit of using OAuth instead of your own basic authentication? OAuth doesn't share password data but instead uses authorization tokens to prove an identity between consumers and service providers

### Terms

**Client ID** s is public code identifier for apps
**Client Secret** is a secret code used by the OAuth Client to Authenticate to the Authorization Server.
**Authentication Endpoint** a REST API's is used to authenticate the users.
**Access Token Endpoint** an HTTP endpoint that micropub clients can use to obtain an access token given an authorization code.
**API Endpoint** URL of a server or service
**Authorization Code** is a temporary code that the client will exchange for an access token
**Access Token** s an opaque string that identifies a user, app, or Page and can be used by the app to make graph API calls

### Preview

##### What is the JSON Web Token structure?

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

Header
Payload
Signature
Therefore, a JWT typically looks like the following.

`xxxxx.yyyyy.zzzzz`

Let's break down the different parts.

- Header
  The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

For example:

```
{
  "alg": "HS256",
  "typ": "JWT"
}
```

Then, this JSON is Base64Url encoded to form the first part of the JWT.

- Payload
  The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.
