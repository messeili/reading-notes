## HTML Links
**Links are found in nearly all web pages. Links allow users to click their way from page to page.**

### HTML Links - Syntax :

**Hyperlinks are defined with the HTML `<a>` tag:**

```<a href="url">link text</a>```
*Also, we can move to a spicifice part of a page by linking with a word has the same Id to refere to that part of the page*
```
<h1 id="top">first heading</h1>
<p><a href="#top">Top</a></p>
```
Using this code gives us a linked word  called top makes us go back to tag that has an Id called top

## HTML Layout :

### Introduction to CSS layout

#### - Normal flow : Elements on webpages lay themselves out according to normal flow - until we do something to change that. This article explains the basics of normal flow as a grounding for learning how to change it.

#### - Positioning : The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky).

**The position property specifies the type of positioning method used for an element.**

**There are five different position values:**

1. `static:An element with position: static; is not positioned in any special way; it is always positioned according to the normal flow of the page.`
2. `relative:An element with position: relative; is positioned relative to its normal position.`
3. `fixed:An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled`
4. `absolute:An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed`
5. `sticky:An element with position sticky; is positioned based on the user's scroll position`

#### Elements are then positioned using the top, bottom, left, and right properties. However, these properties will not work unless the position property is set first. They also work differently depending on the position value.

#### Overlapping Elements : When elements are positioned, they can overlap other elements.

**The `z-index` property specifies the stack order of an element (which element should be placed in front of, or behind, the others).**

#### The float Property :
**The float property is used for positioning and formatting content e.g. let an image float left to the text in a container.**

**The float property can have one of the following values:**

1. left - The element floats to the left of its container
2. right - The element floats to the right of its container
3. none - The element does not float (will be displayed just where it occurs in the text). This is default
4. inherit - The element inherits the float value of its parent

***In its simplest use, the `float` property can be used to wrap text around images.***

### Grid Layout
**The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.**

The grid layout contains six columns and three rows

## JavaScript Functions :
 **A JavaScript function is a block of code designed to perform a particular task.**

**A JavaScript function is executed when "something" invokes it (calls it).**

**Example :**
```
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}
```
### JavaScript Function Syntax :
**A JavaScript function is defined with the `function` keyword, followed by a name, followed by parentheses ().Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).**

**The parentheses may include parameter names separated by commas: (parameter1, parameter2, ...)**
 
**The code to be executed, by the function, is placed inside curly brackets: {}**
```
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}

## JavaScript Function Scope
**In JavaScript there are two types of scope:**
```
1. Local scope
2. Global scope
```
JavaScript has function scope: Each function creates a new scope.Scope determines the accessibility (visibility) of these variables.Variables defined inside a function are not accessible (visible) from outside the function.

## Definition of Pair Programming :
**As the name implies, pair programming is where two developers work using only one machine. Each one has a keyboard and a mouse. One programmer acts as the driver who codes while the other will serve as the observer who will check the code being written, proofread and spell check it, while also figuring out where to go next. These roles can be switched at any time: the driver will then become the observer and vice versa.**

*It’s also commonly called “pairing,” “programming in pairs,” and “paired programming.”*

### Pair Programming Advantages :

1. Two heads are better than one
2. More efficient
3. Fewer coding mistakes
4. An effective way to share knowledge
5. Develops your staff’s interpersonal skills