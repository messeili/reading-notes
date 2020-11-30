# Reading37: Redux - Combined Reducers

## Review, Research, and Discussion

- **Why choose Redux instead of the Context API for global state?**  
  Because it will manage all app state
- **What is the purpose of a reducer?**  
  to receive the action , then proceed depend on it
- **What does an action contain?**  
  An object with a payload and type props
  - **Why do we need to copy the state in a reducer?**  
    because its read only

## Terms

- **immutable state**: unchangeable, read-only
- **time travel in redux**:
- **action creator**:
- **reducer**: functions that take the current state and an action as arguments, and return a new state result.
- **dispatch**: a function of the Redux store that triggers a state change.

## Preview

#### Redux

Redux is a predictable state container for JavaScript apps.

The first principle of Redux is that everything that changes in your application, including the data and the UI state, is contained in a single object, we call the state or the state tree.
