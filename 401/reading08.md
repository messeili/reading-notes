# Reading08: Express Routing & Connected API

## Review, Research, and Discussion

1. Name 3 real world use cases where you'd want to change the request with custom middleware.

- Authentication
- fetch data from different API's.
- Authorization and validation

2. True or false: The route handler is middleware?

False, the middleware becomes before the route handler itself

4. In what ways can a middleware function end the process and send data to the browser?

if not using or passing the `next` parameter

5. At what point in the request lifecycle can you "inject" middleware?
   before sending it

6. What can cause express to error with "Request headers sent twice, cannot start a second response"
   when sending a response twice

### Definitions:

- **Middleware** : functions that have access to the request, the response object, and the next middleware function in the application's request-response cycle. The next middleware function is commonly denoted by a variable named next.

- **Request Object** : An object that represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers.

- **Response Object** : An object that represents the HTTP response that an Express app sends when it gets an HTTP request.

- **Application Middleware** :

- **Routing Middleware** : Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router()..

## Preparation Materials

### Routing

Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing.

You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function (See Using middleware for details).

These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

- `app.use()` : to specify middleware as the callback function
- `app.get()` : to handle GET requests
- `app.post()` : to handle POST requests
- `app.all()` : to handle ALL HTTP requests

### Response Methods

| method           | use of it                                                                             |
| ---------------- | ------------------------------------------------------------------------------------- |
| res.send()       | Send a response of various types.                                                     |
| res.render()     | Render a view template.                                                               |
| res.redirect()   | Redirect a request.                                                                   |
| res.sendFile()   | Send a file as an octet stream.                                                       |
| res.download()   | prompt a file to be downloaded.                                                       |
| res.end()        | End the response process.                                                             |
| res.json()       | Send a JSON response.                                                                 |
| res.sendStatus() | Set the response status code and send its string representation as the response body. |
