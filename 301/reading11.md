# EJS

![ejs image](https://images.g2crowd.com/uploads/product/image/large_detail/large_detail_f9dd821cb48125c63c64b6f5c7552372/ejs.png) 

EJS is templating language that use to generate html files at the end. It used in need to a way to create dynamic content to the web page based on the data coming from the api and OFC we can’t get that goal by static html.

**Install**
It's easy to install EJS with NPM.
```
$ npm install ejs
```

**How to Use**
Pass EJS a template string and some data. BOOM, you've got some HTML.
```
let ejs = require('ejs');
let people = ['geddy', 'neil', 'alex'];
let html = ejs.render('<%= people.join(", "); %>', {people: people});
```
**CLI**
Feed it a template file and a data file, and specify an output file.
```
ejs ./template_file.ejs -f data_file.json -o ./output.html
```
**Browser support**
Download a browser build from the latest release, and use it in a script tag.
```
<script src="ejs.js"></script>
<script>
  let people = ['geddy', 'neil', 'alex'];
  let html = ejs.render('<%= people.join(", "); %>', {people: people});
</script>
```

**Example**
```
<% if (user) { %>
  <h2><%= user.name %></h2>
<% } %>
```
**Usage**
```
let template = ejs.compile(str, options);
template(data);
// => Rendered HTML string

ejs.render(str, data, options);
// => Rendered HTML string

ejs.renderFile(filename, data, options, function(err, str){
    // str => Rendered HTML string
});
```
**Options**
1. <% 'Scriptlet' tag, for control-flow, no output
2. <%_ ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it
3. <%= Outputs the value into the template (HTML escaped)
4. <%- Outputs the unescaped value into the template
5. <%# Comment tag, no execution, no output
6. <%% Outputs a literal '<%'
7. %> Plain ending tag
8. -%> Trim-mode ('newline slurp') tag, trims following newline
9. _%> ‘Whitespace Slurping’ ending tag, removes all whitespace after it