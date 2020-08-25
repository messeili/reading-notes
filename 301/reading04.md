## CSS GRID
The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.

The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be. In this case, for the first argument, I’ve used auto-fill which will create a grid with as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to minmax(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a maximum of 1fr. grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr; will create a grid with 6 columns which are each one fraction unit wide. They each share 1/6 of the width of the container. You could also use
```
grid-template-columns: repeat(6, 1fr);
```
to get the same result. Using the span value with a number will make a grid cell span that many rows, or columns . grid-column: span 2; for example, will create a cell that is two columns wide. I’ve used object-fit again to make the images keep their aspect ratio while filling the space of their containers. If the images in your gallery have more constraints than cat pictures, with regards to the space they’ll fit in then you can use media queries to change the number of rows or columns they span at different widths.
