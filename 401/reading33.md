# Reading33: Context API

## Review, Research, and Discussion

- **Describe use cases for useMemo() and useReducer()**  
  when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.
- **Why do custom hooks need the use prefix?** It's a react convention
- **What do custom hooks usually do?**
- **Using any list of custom hooks, research and name one that you think will be useful in your applications**  
  useAsync
- **Describe how a hook that fetches API data might work**  
   You have to add a closure asyn function that fetch the data from the api

## Terms

- **reducer**: useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks. .

## Preview

#### Context API

In a typical React application, data is passed top-down (parent to child) via props, but this can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.
