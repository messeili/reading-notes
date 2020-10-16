# Reading02: Classes, Inheritance, Functional Programming

## Preview

#### TDD in Js

Test-driven development (TDD) is a technique for ensuring that your code does what you think it does.

TDD is a great way of catching the majority of programming errors. It’s not perfect, of course—in particular, it can’t tell you when your assumptions are wrong—but it’s very good at catching the kinds of bugs JavaScript is prone to.

Context
Context is what the value of this keyword in your code when it is running.

#### Inheritance

JavaScript is a bit confusing for developers experienced in class-based languages (like Java or C++), as it is dynamic and does not provide a class implementation per se (the class keyword is introduced in ES2015, but is syntactical sugar, JavaScript remains prototype-based).

When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.

Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.

#### Classes

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class alike semantics.

```
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  // This method could be used by the class name directly
  static area(height, width) {
    return height * width;
  }
}
```

#### this

A function’s this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.

A property of an execution context (global, function or eval) that, in non–strict mode, is always a reference to an object and in strict mode can be any value.

Global context
In the global execution context (outside of any function), this refers to the global object whether in strict mode or not.

```
console.log(this === window); // true
a = 37;
console.log(window.a); // 37
this.b = 'MDN';
console.log(window.b); // "MDN"
console.log(b); // "MDN"
```

Function context
Inside a function, the value of this depends on how the function is called.

non-strict mode : this will default to the global object, which is window in a browser.

```
function f1() {
  return this;
}
// In a browser:
f1() === window; // true
// In Node:
f1() === globalThis; // true
strict mode : if the value of this is not set when entering an execution context, it remains as undefined

function f2() {
  'use strict'; // see strict mode
  return this;
}
f2() === undefined; // true
```

Class context
The behavior of this in classes and functions is similar, since classes are functions under the hood. But there are some differences and caveats.

Within a class constructor, this is a regular object. All non-static methods within the class are added to the prototype of this:

```
function f2() {
  class Example {
    constructor() {
      const proto = Object.getPrototypeOf(this);
      console.log(Object.getOwnPropertyNames(proto));
    }
    first() {}
    second() {}
    static third() {}
  }
  new Example(); // ['constructor', 'first', 'second']
```

### Why would you want to run JavaScript code outside of a browser?

Running JavaScript without/outside a browser means you are using node.js technology to execute your JavaScript code. This type of usage of javascript typically refers to backend programming where your javascript code will interact with your database and can be used to create RESTful APIs.

### What is the difference between a module and a package?

Modules are libraries for Node.js, Node.js has a simple module loading system. In Node.js, files and modules are in one-to-one correspondence.

A package is one or more modules (libraries) grouped (or packaged) together. These are commonly used by other packages or a project of your own. Node.js uses a package manager, where you can find and install thousands of packages.

also
A module is a single JavaScript file that has some reasonable functionality.

A package is a directory with one or more modules inside of it and a package.json file which has metadata about the package.

### What does the node package manager do?

npm, short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

### Vocabulary Terms

- ecosystem: Managed lifecycle and dependency injection for your application components.
- Node.js Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.
- V8 Engine is an open source runtime engine written in C++.
- module is a single JavaScript file that has some reasonable functionality.
  \*package is a directory with one or more modules inside of it and a package.json file which has metadata about the package.
- node package manager (npm) libraries built by the awesome community which will solve most of your generic problems. npm (Node package manager) has packages you can use in your apps to make your development faster and efficient.
- server: A slave computer with hight performance specifications to run 24/7.

- environment: Set of processes and tools that are used to develop a source code or program.

- interpreter: Program that executes instructions written in a high-level language.

- compiler: Is a special program that processes statements written in a particular programming language and turns them into machine language or “code” that a computer’s processor uses.
