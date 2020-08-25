# Read03: ## Javascript Templating


## Javascript Templating
Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic. The template engine then replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.



## Mustache
logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object. img

Mustache is NOT a templating engine. img



## Flexbox
Since flexbox is a whole module and not a single property, it involves a lot of things including its whole set of properties. Some of them are meant to be set on the container (parent element, known as “flex container”) whereas the others are meant to be set on the children (said “flex items”).

Properties for the Parent (flex container):

display :This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.
flex-direction: laying out either in horizontal rows or vertical columns.
flex-wrap : By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.
flex-flow :This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. The default value is row nowrap.
justify-content.
align-items
align-content

Properties for the Children (flex items):

order
flex-grow
flex-shrink
flex-basis
align-self