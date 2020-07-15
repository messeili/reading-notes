## Objects  

Objects group together a set of variables and function to create a model of a something you would recognize from the real world,

in an objects variables becomes known as properties properties tell us about the object,such as the name of a hotel or the number of rooms it has.

in an objects functions becomes known as methods methods represent tasks that are associated with the object.

Example

```
var hotel = {
  name: "Quay",
  rooms: 40,
  booked: 25,
  gym: true,
  roomTypes: ["twin", "double", "suite"],
  checkAvailability: function () {
    return this.rooms - this.booked;
  },
};
// This is How to accessing an object, properities and methods.
var hotelName = hotel.name;
// This will gives us hotelName = Quay;
var roomesFree = hotel.checkAvalibilty();
// This will execute the function inside the object hotel.
// Another way to access an Object (JUST ITS PROPERTIES).
var hotelRooms = hotel["rooms"];
The code above, you can see name,rooms,booked,gtm, and roomTypes : all of htese are called properties which have KEY and VALUE fro each one. checkAvailability(); called a method.
```

You accessing an Object by using what we call a DOT NOTATION It is shown above in the comments.

## Document Object Model.
The Document object model (DOM) specifies how browsers shuould create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

You can imagin that the HTML page is like a tree, each element has some branches under it all these branched has one parent in the top of it. which it is the <html> tag .
```
<html>
  <body>
    <div id="page">
      <h1 id="header">List</h1>
      <h2>By groceries</h2>
      <ul>
        <li id="one" class="hot"><em>fresh</em></li>
        <li id="two" class="hot">pinenuts</li>
        <li id="three" class="hot">honey</li>
        <li id="four">balsamic vinegar</li>
      </ul>
      <script src="js/list.js"></script>
    </div>
  </body>
</html>
```

The Document Node it represent the entire page (and also correspondes to the document object.), when you access ant element, attribute, or text node you navigate to it via the document node, relationships between the document and all of the element nodes are descibed using the terms as a family tree : Parent,Children,Sibling, Ancestors, and Descendants.

The Element Nodes HTML elements describe the structure of an HTML page, to access the DOM tree, you should start by looking for elements, then you can access its text and attribute nodes if you want to.

The Attribute Nodes Attribute nodes are not children of the element.

Text Nodes Once you have accessed an element node, you can then reach the text within that element

## Working with the DOM tree.
Access the elements : you can access any element in the DOM by using these selectors:
```
getElementById(id name) : Used to select an element with a specific id.
getElementsByClassName(class name) : Used to select all elements that have that class name as an attribute (Returns an array of elements), to select one of the items you can use the **item(index)** method or you can access it just like an array.
parentNode: select the parent of the current element node.
previousSibling/nextSibling: select the previous of next sibling of the DOM tree.
firstChild/lastChild: select the first child of the last of the current element.
querySelector(): Uses a CSS selector, and returns the first matching element.
getElementsByTagName(tag name) : select all elements that have this tag name.
querySelectorAll(): Uses a CSS selector to select all matching elements.
Work with those elements.
Access/Update Text nodes
nodeValue :This property lets you access or update contents of a text node.
Work with HTML content
innerHTMl : allows to access child elements and text content.
textContent : same as innerHTML.
createElement()/createTextNode() : this method let you create new nodes.
appendChild()/removeChild() : Add nodes to a tree/ remove nodes from a tree.
Access or Update Attribute values
hasAttribute() : checks if the attribute exists.
getAttribute() : get the value of an attribute.
setAttribute() : update the value.
removeAttribute() : removes the attributes.
Cross-site Scripting (XSS) attacks.
if you add HTML to a page using inerHTML (or several jQuery methods), you need to be aware of Cross-Site-Scripting Attacks or XSS, other wise an attacker could gain access to your users' accounts.
```
##Why problem domains are hard
The big issue is that many problem domains are like a puzzle with a blurry picture or no picture at all.you can’t really see what you are trying to build very clearly, The same thing happens when writing code. Writing code is a lot like putting together a jigsaw puzzle. We put together code with the purpose of building components that we have taken out of the “bigger picture” of the problem domain.

##Programming is easy if you understand the problem domain.
understanding the problem is the most critical piece to the equation. It is very difficult to solve a problem before you know the question. It’s like buzzing in on Jeopardy before you hear the clue and shouting out random questions.
