# Reading01: Node Ecosystem, TDD, CI/CD

## Preview:

Node and npm
Node
node.js is a JavaScript runtime ( includes everything you need to execute a program) built on Chrome’s V8 JavaScript engine. it uses asynchronous programming.

npm
npm is the world’s largest software registry. Open source developers from every continent use npm to share and borrow packages.

you can use it to:

Adapt packages of code for your apps, or incorporate packages as they are.
Download standalone tools you can use right away.
Run packages without downloading.
Share code with any npm user.
Restrict code to specific developers.
Create (organizations) to coordinate package maintenance, coding, and developers.
Manage multiple versions of code and code dependencies.
Update applications easily when underlying code is updated.
Discover multiple ways to solve the same puzzle.
Find other developers who are working on similar problems and projects.

## Review, Research, and Discussion:

### 1. Array.map()

The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

### 2. Array.reduce()

The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in single output value.

### 3.How to use superagent()

is a light-weight, flexible and expressive Ajax library.

**using async/await**

```
async function getFromApi(cityName){
  let result = await superagent.get(`https://geocode.xyz/${cityName}?json=1`)
  console.log(result.body.latt,',',result.body.longt)
}

getFromApi('amman')
```

**using .then**

```
function getFromApi(cityName){
  superagent.get(`https://geocode.xyz/${cityName}?json=1`).then(results=>{
  console.log(results.body.latt,',',results.body.longt)

  })
}

getFromApi('amman')
```

### 4.Promises()

A promise is an object that wraps an asynchronous operation and notifies when it’s done. This sounds exactly like callbacks, but the important differences are in the usage of Promises. Instead of providing a callback, a promise has its own methods which you call to tell the promise what will happen when it is successful or when it fails. The methods a promise provides are “then(…)” for when a successful result is available and “catch(…)” for when something went wrong.
There are lots of frameworks for creating and dealing with promises in JavaScript, but all of the examples below assumes that we are using native JavaScript promises as introduced in ES6.

### 5.Are all callback functions considered to be Asynchronous? Why or Why Not?

No. Only input and output functions are usually asynchronous, but many other callbacks are synchronous.
