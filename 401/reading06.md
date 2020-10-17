# Reading06: HTTP and REST

## Review, Research, and Discussion

Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.

##### What is the advantage of an ORM, like Mongoose?

Productivity
Application design
Code Reuse
Application Maintainability

##### How does the repository pattern compare with an ORM?

Repositories deal with Domain/Business objects
ORM handles db objects.
When making a repository/facade, what flexibility do you gain? Facades serve as “static proxies” to underlying classes in the service container, providing the benefit of a terse, expressive syntax while maintaining more testability and flexibility than traditional static methods.

##### Name 3 cloud based NoSQL Databases

Azure Cosmos DB..
Amazon DynamoDB.
MongoDB.

#### Document the following Vocabulary Terms

1. lifecycle:the series of changes in the life of an organism including reproduction.

2. collections: collection is a class used to represent a set of similar data type items as a single unit.

3. “Repository” design pattern:is a kind of container where data access logic is stored.

4. mongoose middleware:functions which are passed control during execution of asynchronous functions.

5. Object Relation Mapping (ORM):programming technique for converting data between incompatible type systems using object-oriented programming languages.

## Preview

HTTP stands for Hypertext Transfer Protocol. It’s a stateless, application-layer protocol for communicating between distributed systems, and is the foundation of the modern web.

HTTP Basics
HTTP allows for communication between a variety of hosts and clients, and supports a mixture of network configurations.

This makes HTTP a stateless protocol. The communication usually takes place over TCP/IP, but any reliable transport can be used. The default port for TCP/IP is 80, but other ports can also be used.

Communication between a host and a client occurs, via a request/response pair. The client initiates an HTTP request message, which is serviced through a HTTP response message in return. We will look at this fundamental message-pair in the next section.

REST is acronym for REpresentational State Transfer. It is architectural style for distributed hypermedia systems and was first presented by Roy Fielding in 2000 in his famous dissertation.

REST and HTTP are not same because REST also intends to make the web (internet) more streamline and standard, he advocates using REST principles more strictly. And that’s from where people try to start comparing REST with web (HTTP).

Resource Methods
Important thing associated with REST is resource methods to be used to perform the desired transition. A large number of people wrongly relate resource methods to HTTP GET/PUT/POST/DELETE methods.
