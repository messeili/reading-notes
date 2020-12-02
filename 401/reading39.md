# Reading38: Redux - Combined Reducers

## Review, Research, and Discussion

- **How granular should your reducers be?**  
  **Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched**  
   con
- **Name a strategy for preventing the above**

## Terms

- **store**: An object with a few methods on it that holds the whole state tree of the application.
- **combined reducers**: A helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

## Preview

#### Async Logic and Data Fetching

By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

#### Redux Async Data Flow

![img](https://redux.js.org/assets/images/ReduxAsyncDataFlowDiagram-d97ff38a0f4da0f327163170ccc13e80.gif)
