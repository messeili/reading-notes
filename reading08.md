# Layouts

## Controlling the position of elements
* Static:  
In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:
position: static  
* Relative:
Relative positioning moves an element in relation to where it would have been in normal flow.
For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right.
You can indicate that an element should be relatively positioned using the position property with a value of relative  
* absolute:
When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.) 
The box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element.  
* fixed: Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.
It positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place. It is a good idea to try this example in your browser to see the effect.  
##Screen sizes:
Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.

## Screen resolution:  
Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens. 

## Fixed and Liquid layouts
![read8-1](https://github.com/messeili/reading-notes-201/blob/master/img/read8-1.PNG)
![read8-2](https://github.com/messeili/reading-notes-201/blob/master/img/read8-2.PNG)  


## Layout grids
![read8-3](https://github.com/messeili/reading-notes-201/blob/master/img/read8-3.PNG)
 

## Css frameworks
advantages
They save you from repeatedly writing code for the same tasks.
They will have been tested across different browser versions (which helps avoid browser bugs).
disadvantages
They often require that you use class names in your HTML code that only control the presentation of the page (rather than describe its content).
In order to satisfy a wide variety of needs, they often contain more code than you need for your particular web page (commonly referred to as code “bloat”).
One of the most popular uses of CSS frameworks is in creating grids to layout pages. There are several grid frameworks out there, but the one we will be looking at over the next few pages is the 960 Grid System (available at www.960.gs).
960.gs provides a style sheet that you can include in your HTML pages. Once our page links to this style sheet, you can provide the appropriate classes to your HTML code and it will create multiple column layouts for you. The 960.gs website also provides templates you can 
download to help design your pages using a 12 column grid. (In addition, there is a variation on the grid that uses 16 columns.)
To create a 12 column grid, an element that contains the entire page is given a class attibute whose value is container_12. This sets the content of the page to be 960 pixels wide and indicates that we are using a 12 column grid.
There are different classes for blocks that take up 1, 2, 3, 4, and up to 12 columns of the grid. Each block uses class names 
such as grid_3 (for a block that stretches over three columns), grid_4 (for a block that stretches over 4 columns) and and so on through to grid_12 (for a box that is the full width of the page). These columns all float to the left, and there is a 10 pixel margin to the left and the right of each one.

