# Read02: jQuery

![js image](https://www.webdesignerdepot.com/cdn-origin/uploads/2019/07/featured_jquery.jpg)

## JQuery

jquery its a JavaScript library let you find the element and the css style then apply your methods or function easily.

WHY USE JQUERY?
JQuery makes coding simpler.

## JQuery methods

to pick an element we use `$` to, e.g.:

```
1. `$('li')`
2. `$('#nameOfTheID')`
3. `$('#nameOfTheclass')`
```

## checking the Readiness

.ready() method checks that the page is ready for your code code to work with.

```
`$(document).ready(...){ }`
```

## GETTING ELEMENT CONTENT

The • htm 1 () and • text () methods both retrieve and update the content of elements. This page will focus on how to retrieve element content.

. html()
is used to retrieve information from a jQuery selection, it retrieves only the HTML inside the first element in the matched set, along with any of its descendants.
. text() it returns the content from every element in the jQuery selection, along with the text from any descendants.

. remove() This method removes all of the elements in the matched set.

## Inserting new elements involves two steps:

1. Create the new elements in a jQuery object

2. Use a method to insert the content into the page
   .before() This method inserts content before the selected element(s).
   .after() This method inserts content after the selected element(s).
   .prepend() This method inserts content inside the selected element(s), after the opening tag.
   .append() This method inserts content inside the selected element(s), before the closing tag.

## How to include JQuery in our page

Load it from CDN:

```
`<script src="//ajax .googl eapi s .com/ ajax/l i bs/ jquery/ 1.10. 2/ jquery .min. js "> </ script>`
```
