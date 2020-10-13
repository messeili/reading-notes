# Reading03: Data Modeling & NoSQL Databases

## Questions:

##### Name 3 advantages to Test Driven Development

1. Better program design and higher code quality
2. Detailed project documentation
3. TDD reduces the time required for project development

##### In what case would you need to use beforeEach() or afterEach() in a test suite?

npm, short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

##### What is one downside of Test Driven Development

It’s difficult to write good tests that cover the essentials and avoid the superfluous.
It takes time and effort to maintain the test suite – it must be reconfigured for maximum value.
If the design is changing rapidly, you’ll need to keep changing your tests. You could end up wasting a lot of time

##### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

Classes can’t be called without new, but functions intended as constructors can (and their this will be wrong)

Classes can extend more types than constructors can (like functions and arrays)

Classes’ prototypes are their parents (they inherit static properties)

Non-classes can’t extend classes because they can’t call the parent constructor

##### Name a use case for a static method

##### Write an example of a Higher Order function and describe the use case it solves

## Vocabulary Terms

- functional programming
  Functional programming languages are specially designed to handle symbolic computation and list processing applications.

- pure function
  A pure function’s return value is based only on its inputs and has no other dependencies or effects on the overall program.

- higher-order function
  A function that can take another function as an argument or returns a function as a result.

- immutable state
  An object who state cannot be modified after it is created.

- object
  Objects are containers for named values called properties or methods.

- object-oriented programming (OOP)
  OOP refers to a type of programming in which we define the data-type of a data-structure, and also the types of operations (methods) that can be applied to the data-structure.

- class
  A class is a type of function, but instead of using the keyword function to initiate it, we use the keyword class, and the properties are assigned inside a constructor() method.

- prototype
  All JavaScript objects inherit properties and methods from a prototype.

- super
  The super keyword is used to access and call functions on an object's parent.

- inheritance
  In simple terms, inheritance is the concept of one thing gaining the properties or behaviors of something else. To say A inherits from B, is saying that A is a type of B.

- constructor
  A constructor is a function that creates an instance of an object.

- instance
  An instance means a reference to an object created by the new keyword.

- context
  Refers to the scope of this.

- this
  Refers to the object it belongs to.

- Test Driven Development (TDD)
  TDD is the act of first deciding what you want your program to do, formulating a failing test, then writing the code to make that test pass.

- Jest
  Jest is a JS library for creating, running, and structuring tests.

- Continuous Integration (CI)
  The practice of creating frequent and isolated changes in code, which are immediately tested and reported on when they are added to a larger code base.

- unit test
  A unit test is designed to test an individual function or library in your code.

## Preparation Materials

### SQL vs NoSQL

| DB  | SQL                                                                                                                                                                                                                                                   | NoSQL                                                                                                                                                                                            |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | SQL databases are primarily called as Relational Databases (RDBMS)                                                                                                                                                                                    | NoSQL database are primarily called as non-relational or distributed database.                                                                                                                   |
| 2   | SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data | NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.               |
| 3   | SQL databases have predefined schema                                                                                                                                                                                                                  | NoSQL databases have dynamic schema for unstructured data.                                                                                                                                       |
| 4   | SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware.                                                                                  | NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.                                                                                      |
| 5   | SQL databases uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful.                                                                                                                                  | In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database. |
| 6   | SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL.                                                                                                                                                                                    | NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb                                                                                                  |
