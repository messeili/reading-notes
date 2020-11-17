# Reading27: Props and State

## Review, Research, and Discussion

- **Can a parent component access the state of a child component?**  
  no
- **What can be passed along in a prop variable?**  
  methods and variables
- **How can a child component “know” the state of another component??**  
  we can get hte state with props to the parent then from the parent to the child

## Terms

- **component props**: component properties that can be passed to other components
- **component state**: object that is managed inside the component itself
- **application state**: interface between your data from any kind of backend or local change and the representation of this data with UI-elements in the frontend.

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
