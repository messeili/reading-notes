# Reading27: Props and State

## Review, Research, and Discussion

- **Does a deployed React application require a server?**  
  No
- **Why do we prefer to test a React application at the behavior rather than the unit level?** Testing components that are not purely functional and are responsible for behavior isn’t difficult, but there aren’t as many resources on the web that describe how to do this.
- **What does npm run build do?**  
  npm run build does nothing unless you specify what “build” does in your package.
- **Describe the actual composition / architecture of a React application**

## Terms

- **BDD**: behavior-driven development
- **Acceptance Tests**: technique performed to determine whether or not the software system has met the requirement specifications.
- **mounting**: process by which the operating system makes files and directories on a storage device
- **build**: process of converting source code files into standalone software artifact(s) that can be run on a computer

## Preview

##### React Props

React Props are like function arguments in JavaScript and attributes in HTML.

To send props into a component, use the same syntax as HTML attributes:

Example Add a "brand" attribute to the Car element:

```
const myelement = <Car brand="Ford" />;
```

The component receives the argument as a props object:

Example Use the brand attribute in the component:

```
class Car extends React.Component {
  render() {
    return <h2>I am a {this.props.brand}!</h2>;
  }
}
```

##### React components has a built-in state object.

The state object is where you store property values that belongs to the component.

When the state object changes, the component re-renders.

Creating the state Object The state object is initialized in the constructor:

Example: Specify the state object in the constructor method:

```
class Car extends React.Component {
  constructor(props) {
    super(props);
    this.state = {brand: "Ford"};
  }
  render() {
    return (
      <div>
        <h1>My Car</h1>
      </div>
    );
  }
}
```
