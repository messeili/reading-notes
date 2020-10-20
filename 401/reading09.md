# Reading08: Express Routing & Connected API

## Review, Research, and Discussion

1. How does route prefixing work with an external routing module?

2. When routing, what's the difference between app.get('/data/:id') and app.get('/data/:name')?
   The parameter name
3. Explain how Express handles routing conflicts?
   will keep looking until finding a valid route
4. What are the ways that a browser can send "data" or request
   forms

## Terms

- **Routing**: How an application's endpoints (URIs) respond to client requests.
- **Route Prefixing**: Is a concept to make the route function that receive same prefix of different requests.
- **Request "Body"**: Data sent by the client to your API.
- **Request "Query"**: This property is an object containing a property for each query string parameter in the route.
- **Request "Params"**: This property is an object containing properties mapped to the named route "parameters".

## Preview

### router.param(name, callback)

Adds callback triggers to route parameters, where name is the name of the parameter and callback is the callback function.

The parameters of the callback function are:

- the request object.
- the response object.
- indicating the next middleware function.
- The value of the name parameter.
- The name of the parameter.

### mongoose middlewares

Mongoose has 4 types of middleware: document middleware, model middleware, aggregate middleware, and query middleware and they all support post and pre hooks.

#### Types of Middleware

- document middleware
- model middleware
- aggregate middleware
- query middleware.

### mongoose virtual joins

Using mongoose virtual joins, you can define more sophisticated relationships between documents.
If you want populate virtual joins to show up when using functions that rely on JSON.stringify(), like Express' res.json() function, set the virtual joins: true option on your schema's toJSON options.
