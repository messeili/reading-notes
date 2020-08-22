# What is CSS??
> 
We can define the CSS its the way how the content will display, such as background color text color text type and many other things. to understanding how CSS works is to imagine that there is an invisible box around every HTML element.  
  
  ![pic](https://www.geeksforgeeks.org/wp-content/uploads/CSS-768x256.png)

## Linking Style Sheets to HTML
Styles can be linking to an HTML document using one of three methods:

1. Inline Style

2. Embedded Style

3. External Style

## How do you connect a CSS styling sheet to an HTML page ?

### 1. Inline Style
Inline Style is the simplest method of adding CSS styles to your HTML pages. An inline style is applied to an HTML document via its style attribute to specific tags within the document,

For example, If you want to add styles to < p > then you can code like this:
```
<p style="color: #0000FF">...<p>
```

### 2. Embedded Style
Embedded Styles allow you to implement any number of CSS styles by placing them between the opening and closing style tags.
```
<style>......</style>
```
You can place Style Tag within the < head > ... < /head > section, just after the < title > tag of your HTML page.
```
<head>
  <style>
    ........
    ........
  </style>
</head>
``` 

### 3. External Style
An external style sheet is a plain text file that contain CSS Style formats only. The extension of the external file should end with .css extension (e.g. pagestyle.css). This external file is referred to as an external style sheet.

The external Style Sheet (.css file) always seperate from HTML file. You can link this external file (.css file) to your HTML document file using the < link > tag . You can place this < link > tag Within the < head > section, and after the < title > element of your HTML file.
```
<link rel="stylesheet" type="text/css" href="styles.css" />
```
The value of the rel attribute must be style sheet. The href attribute indicates the location and name of the style sheet file. In the above code , external file name is "style.css" and it is stored in the same directory location of your HTML file. If you want to store .css file in another directory location, then you should specify the path of your css file in the href.


# understanding Color
Every color on a computer screen is created by mixing amounts of red, green, and blue. To find the color you want, you can use a color picker.  

## Ways to declare the colors
**RGB Values**
Values for red, green, and blue are expressed as numbers between 0 and 255. 

**Hex Codes**
Hex values represent values for red, green, and blue in hexadecimal code

**ColoR Names**
Colors are represented by predefined names. However, they are very limited in number.

## CSS3 has introduced an extra value for RGB colors to 
indicate opacity. It is known as RGBA.
