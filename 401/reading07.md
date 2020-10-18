# Reading07: Express

## Review, Research, and Discussion

##### What’s the difference between PUT and PATCH?

Put updates a full item data including id, patch updates some of the data.

##### Provide links to 3 services or tools that allow you to “mock” an API for development like json-server

Firebase
Postman
Swagger

##### Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

It’s difficult to write good tests that cover the essentials and avoid the superfluous.
It takes time and effort to maintain the test suite – it must be reconfigured for maximum value.
If the design is changing rapidly, you’ll need to keep changing your tests. You could end up wasting a lot of time

##### Compare and contrast SOAP and ReST

### Vocabulary Terms

- SOAP : is an acronym for Simple Object Access Protocol. It is an XML-based messaging protocol for exchanging information among computers. SOAP is an application of the XML specification.

- ReST Verbs : HTTP methods PUT,POST,GET,PATCH,DELETE,OPTIONS

- CRUD Verbs : Create:POST, Read:GET, Update:PUT/PATCH, Delete:DELETE

- Swagger : is in essence an Interface Description Language for describing RESTful APIs expressed using JSON.

## Preparation Materials

Middleware
Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

Middleware functions can perform the following tasks:

Execute any code.
Make changes to the request and the response objects.
End the request-response cycle.
Call the next middleware function in the stack.
