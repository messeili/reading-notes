# Reading01: Node Ecosystem, TDD, CI/CD
  

### 1. Array.map()
The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
`````
let newArray = arr.map(callback(currentValue[, index[, array]]) {
  // return element for newArray, after executing something
}[, thisArg]);

`````

### 2. Array.reduce()
The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in single output value.
````
arr.reduce(callback( accumulator, currentValue[, index[, array]] ) {
  // return result from executing something for accumulator or currentValue
}[, initialValue]);
````
### 3.How to use superagent()
Small progressive client-side HTTP request library, and Node.js module with the same API, supporting many high-level HTTP client features.

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

Unlike other core languages like Java, javaScript works in a single thread, that’s mean each line should be finished in the stack so we can render all the code, but calling data from an outside source (API) may take some time (longer than rendering the code itself), so it will cause some problems in the website especially if some of the code pieces was depending in the data returning.

Here comes the promises job, whenever we want to get data from outside source, another thread will be created for that calling,working parallel to the main thread.

### 5.Are all callback functions considered to be Asynchronous? Why or Why Not?

