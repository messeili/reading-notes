# Reading29: Routing

## Review, Research, and Discussion

- **Do child components have direct access to props/state from the parent?**  
  No
- **When a component “wraps” another component, how does the child component’s output get rendered?**

- **Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?**  
  no
- **What trick can a parent use to share all props with it’s children**

## Terms

- **props.children**: it is used to display whatever you include between the opening and closing tags when invoking a component.
- **composition**: build components from other components.

## Preview

##### The Router

When starting a new project, you need to determine which type of router to use. For browser based projects, there are <BrowserRouter> and <HashRouter> components. The <BrowserRouter> should be used when you have a server that will handle dynamic requests (knows how to respond to any possible URI), while the <HashRouter> should be used for static websites (where the server can only respond to requests for files that it knows about).

Usually it is preferable to use a <BrowserRouter>, but if your website will be hosted on a server that only serves static files, then the <HashRouter> is a good solution.

For our project, we will assume that the website will be backed by a dynamic server, so our router component of choice is the <BrowserRouter>.

History Each router creates a history object, which it uses to keep track of the current location 1 and re-render the website whenever that changes. The other components provided by React Router rely on having that history object available through React’s context, so they must be rendered as descendants of a router component. A React Router component that does not have a router as one of its ancestors will fail to work.

If you are interested in learning more about the history object (I think that this is important), you can check out my blog post A Little Bit of History.

Rendering a <Router> Router components only expect to receive a single child element. To work within this limitation, it is useful to create an <App> component that renders the rest of your application. Separating your application from the router is also useful for server rendering because you can re-use the <App> on the server while switching the router to a <MemoryRouter>.

```
import { BrowserRouter } from 'react-router-dom';

ReactDOM.render((
  <BrowserRouter>
    <App />
  </BrowserRouter>
), document.getElementById('root'));
```
