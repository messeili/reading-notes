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

##### React Hooks

When and why we should use hooks?

1. Huge components that are hard to refactor and test.
1. Duplicated logic between different components and lifecycle methods.
1. Complex patterns like render props and higher-order components.

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
