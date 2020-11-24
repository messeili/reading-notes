# Reading32: Custom Hooks

## Review, Research, and Discussion

- **What does a component’s lifecycle refer to?**  
  Tracing when the component did mounted of updated or ven removed
- **Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect**  
  Because sometimes you forced to pass a value in that function which will lead to invoke that function immediately
- **Why are functional components preferred over class components?**  
  functional component using the hooks will make the code cleaner and more modular
  - **What is wrong with the following code?**  
    It's not allowed to use the hooks inside a loop or conditional statement

## Terms

- **state hook**: a function that add a state to a functional components.
- **effect hook**: A function that will run after the component renders.
- **reducer hook**: a function that lets you optimize performance for components that trigger deep updates.

## Preview

#### UseReducer

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
