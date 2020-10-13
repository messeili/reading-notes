# Reading04: Data Modeling & NoSQL Databases

## Review, Research, and Discussion

In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

- Why would a developer choose to make data models?
  Simply to organize elements of data and standardize the relations between data
- What purpose do CRUD operations serve?
  create, read, update and delete, four basic functions that manipulate a database.
- What kind of database is Postgres? What kind of database is MongoDB?
  Postgres in a SQL based Database, where Mongo is a NoSQL Database.

- What is Mongoose and why do we need it?
  Mongo is a document-oriented NoSQL database used for high volume data storage

## Vocabulary Terms

- database
  is an organized collection of structured information, or data, typically stored electronically in a computer system

- data model
  is an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.

- CRUD
  create, read, update and delete, four basic functions that manipulate a database.

- schema
  the skeleton structure that represents the logical view of the entire database.

- sanitize
  The process of disposing the data securely when it reached the end of its life or is deemed trivial.

- Structured Query Language (SQL)
  Structured Query Language) is a domain-specific language used in programming and designed for managing data held in a relational database management system (RDBMS).

- Non SQL (NoSQL)
  Non-relational database

- MongoDB
  is a document-oriented NoSQL database used for high volume data storage
- record
  is a database entry that may contain one or more values.
- document
  is a modern way to store data in JSON format rather than simple rows and columns

- Object Relation Mapping (ORM)
  is a programming technique for converting data between relational databases and object oriented programming languages

## Preparation Materials

### Repository Design Pattern

A Repository mediates between the domain and data mapping layers, acting like an in-memory domain object collection. Client objects construct query specifications declaratively and submit them to Repository for satisfaction. Objects can be added to and removed from the Repository, as they can from a simple collection of objects, and the mapping code encapsulated by the Repository will carry out the appropriate operations behind the scenes.”

Repository pattern separates the data access logic and maps it to the business entities in the business logic. Communication between the data access logic and the business logic is done through interfaces.

![img1](https://cubettech.com/wp-content/uploads/2015/07/Reposiory-Design-Pattern.png)

### In Memory Database Testing

he in memory database turned out to be perfect to test applications where the logic is mainly handled through database operations and where the memory and execution time are not an issue.
