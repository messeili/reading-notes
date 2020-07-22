## Chapter 5 HTML book Images.

There are many reasons why you might want ro add an image to a web page, you might want to include a logo, photograph, illustration, diagram, or chart.

If you are building a site from scratch, it is good practice to create a folder for all of the images the site uses. As a website grows, keeping images in a separate folder helps you understand how the site is organized. Images should be :

- Be relevant
- Convy information
- Convey the right mood
- Be instantly recognisable
- Fit the color palette


`src`: This tells the browser where
it can find the image file. This will usually be a relative URL pointing to an image on your own site.

`alt`:This provides a text description of the image which describes the image if you cannot see it.

`title` : You can also use the title attribute with the `<img>`element to provide additional information about the image.

`align` : tou can choose between left,right,middle,bottom,and top.

it is really rocmended that you should place it at :

- before a paragraph The paragraph starts on a new line after the image.
- InsIde the start of a paragraph
  The first row of text aligns with the bottom of the image.
- In the mIddle of a paragraph
  The image is placed between the words of the paragraph that it appears in.

### Three rules to create a picture.

1.  Save the images in the right format , jpeg,gif, or png formats.
2.  Save the images at the right size
3.  Use the correct resolution.



## HTML Tables.

There are several types of information that need to be displayed in a grid or table. such as : sports resutl, stock, reports ... etc.

**Example :**

```html
<html>
  <head>
    <title>Tables</title>
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th></th>
          <th scope="col">Home starter hosting</th>
          <th scope="col">Premium business hosting</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Disk space</th>
          <td>250mb</td>
          <td>1gb</td>
        </tr>
        <tr>
          <th scope="row">Bandwidth</th>
          <td>5gb per month</td>
          <td>50gb per month</td>
        </tr>
        <!-- more rows like the two above here -->
      </tbody>
      <tfoot>
        <tr>
          <td></td>
          <td colspan="2">Sign up now and save 10%!</td>
        </tr>
      </tfoot>
    </table>
  </body>
</html>
```
```
<html>
 <head>
 <title>Tables</title>
 </head>
 <body>
 <table>
 <thead>
 <tr>
 <th></th>
 <th scope="col">Home starter hosting</th>
 <th scope="col">Premium business hosting</th>
   </tr>
 </thead>
 <tbody>
 <tr>
 <th scope="row">Disk space</th>
 <td>250mb</td>
 <td>1gb</td>
 </tr>
 <tr>
 <th scope="row">Bandwidth</th>
 <td>5gb per month</td>
 <td>50gb per month</td>
 </tr>
<!-- more rows like the two above here -->
 </tbody>
 <tfoot>
 <tr>
 <td></td>
 <td colspan="2">Sign up now and save 10%!</td>
 </tr>
 </tfoot>
 </table>
 </body>
</html>
```

`<table>` : a table tag which contain all the table tags.

`<thead>` : tells the browser that inside this tage is the table head.

`<tbody>` : tells the browser that inside this tage is the table body.

`<tr>` : table row.

`<th>` : table head data.

`<td>` : table data.

`<tfoot>` : The footer belongs inside the `<tfoot>` element.

---

## Chapter 12 HTML book Text.

There is 3 main types of default fonts in general.

- Serif : <p style="font-family: serif; ">Serif fonts have extra details on the ends of the main strokes of the letters. These details are known as serifs</p>.

- Sans-serif : <p style ="font-family: sans-serif;">Sans-serif fonts have straight ends to letters, and therefore have a much cleaner design.</p>

- Monospace : <p p style ="font-family: monospace;">Every letter in a monospace (or fixed-width) font is the same width. (Non-monospace fonts have different widths.)</p>

These fonts and many others are installed in your computer by default, but what if i want to use a font that is not intalled?

```css
@font-face {
  font-family: "ChunkFiveRegular";
  src: url("fonts/chunkfive.eot");
}
h1,
h2 {
  font-family: ChunkFiveRegular, Georgia, serif;
}
```

as shown above you can use something called `@font-face` this makes you define a new font family with its url and source, then you can use it freely in any selector you want.

Some important properties for text :

`font-weight : bold/normal` : it makes your text <span style="font-weight : bold">bold</span> ir normal.

`font-style : normal/italic/oblique` : it makes your text appear normal, <span style="font-style : italic">italic</span>, and <span style="font-style : obliqu">obliqu</span>

`text-transform : uppercase/lowercase/capitalize` it makes you text , <span style = "text-transform : uppercase" > uppercase</span> , <span style = "text-transform : lowercase" > LOWERCASE</span> , <span style = "text-transform : capitalize" > capitalize</span>.

`text-decoration : none/underline/overline/line-through/blink` it makes you text , <span style = "text-decoration: none" > none</span> , <span style = "text-decoration : underline" > underline</span> , <span style = "text-decoration : overline" > overline</span>,
<span style = "text-decoration: line-through" > line through</span> , <span style = "text-decoration : blink" > blink</span>

`line-height` : take a unit like 5px of 1.5 just like WORD , it gives a space between each line.

`letter-spacing/word-spacing` : <span style = "letter-spacing: 5px" > letter spacing</span>

<span style = "word-spacing: 5px" > This Text has normal space</span>

`text-align: left/right/justify/center` :

<p style = "text-align: left" > This Text has left align</p>  
<p style = "text-align: right" > This Text has right align</p>  
<p style = "text-align: center" > This Text has center align</p>  
<p style = "text-align: justify" > This Text has justify align</p>

`text-shadow` :

<p style = "background-color: #cccccc;
color: #ffffff;
text-shadow: 2px 2px 7px #111111;" > This Text has shadow </p>