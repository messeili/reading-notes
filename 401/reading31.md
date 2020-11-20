# Reading31: Hooks API

## Review, Research, and Discussion

- **Why do we not need more .html pages in a multi-page React app?**  
  Because we are following the SPA (single page application)
- **If we wanted a component to show up on every page, where would we put it and why?**  
  Inside the <BrowserRouter />, outside a <Route />
- **What does props.children contain?**  
  Whatever included between the opening and closing tags when invoking a component.

## Terms

- **Composition**: The process of building components from other components.
- **Children / Child Components**: a components inside other components that can be accessed throw props.children
- **Hash Routing**: doing something in response to a change in the browser’s current URL using the portion of the page’s URL starting with #
- **Link Routing**:

## Preview

#### React Hooks

Hooks are a new addition in React 16.8. They let you use state and other React features without writing a class.

What is a Hook? A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

When and why we should use hooks?

1. Huge components that are hard to refactor and test.
1. Duplicated logic between different components and lifecycle methods.
1. Complex patterns like render props and higher-order components.

##### State Hook

###### Declaring a State Variable

In a class, we initialize the count state to 0 by setting this.state to `{ count: 0 }` in the constructor:

```
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }
```

In a function component, we have no this, so we can’t assign or read this.state. Instead, we call the useState Hook directly inside our component:

```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

```

What does calling useState do? It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

##### Effect Hook

The Effect Hook lets you perform side effects in function components, you can think of `useEffect` Hook as `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` combined.
