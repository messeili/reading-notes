## HTML5 video and audio
The ```<video>``` and ```<audio>``` elements allow us to embed video and audio into web pages. As we showed in Video and audio content, a typical implementation looks like this:
```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```
This creates a video player inside the browser.

## Images
CSS Setting height and width for images the height and width properties are used to set the height and width of an element.

The `height` and `width` properties do not include padding, borders, or margins. It sets the height/width of the area inside the padding, border, and margin of the element.

```
img {
height: 200px;
width: 50%;
}
```

**How to align images Side By Side**

**Example :**
```
.column {
float: left;
width: 33.33%;
padding: 5px;
}

.row::after {
content: "";
clear: both;
display: table;
}
```
**CSS background-image**

The `background-image` property specifies an image to use as the background of an element.

**Add Responsiveness**

Optionally, you could add media queries to make the images stack on top of each other instead of floating next to each other, on a specific screen width.



