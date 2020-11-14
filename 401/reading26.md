# Reading26: Component Based UI

## Review, Research, and Discussion

- **Name 5 Javascript UI Frameworks (other than React)**

1. Angular
1. Vue
1. Ember
1. Meteor
1. Node.js

- **What’s the difference between a framework and a library?** Frameworks and libraries are both code written by someone else that helps you perform some common tasks in a less verbose way. A framework inverts the control of the program. It tells the developer what they need. A library doesn’t. The programmer calls the library where and when they need it.

## Terms

- **Rendering** is the process of displaying something on a screen. If one wishes the user to see a visual representation of some result in a program, it must be rendered in some form or fashion be it text, graphics, etc
- **Templates** a gauge, pattern, or mold for a code or framework
- **State** The state object is where you store property values that belongs to the component. When the state object changes, the

## Preview

##### React

React. js is an open-source JavaScript library that is used for building user interfaces specifically for single-page applications.React allows developers to create large web applications that can change data, without reloading the page. The main purpose of React is to be fast, scalable, and simple.

##### JSX

JSX is a syntax extension to JavaScript. It's recommended to be used with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.

- **Embedding Expressions in JSX**  
  In the example below, we declare a variable called name and then use it inside JSX by wrapping it in curly braces:

```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```

- **Rendering an Element into the DOM**  
  To render a React element into a root DOM node, pass both to `ReactDOM.render()`:

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
