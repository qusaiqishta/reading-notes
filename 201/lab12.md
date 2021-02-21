# chart.JS

Javascript provided many charts that you can adds to your web page to clearify the data inside it such as bar charts, line charts, pie charts and more. At first you need to download library called chart.js then used *canvas* tag inside HTML file


&nbsp;

#  Canvas Element
The HTML (canvas) element is used to draw graphics, on the fly, via JavaScript.

The (canvas) element is only a container for graphics. You must use JavaScript to actually draw the graphics.

### Note that a canvas is a rectangular area on an HTML page. By default, a canvas has no border and no content. So you have to specify the width and height of that border like in the following example:

```
<canvas id="myCanvas" width="200" height="100"></canvas>
```


## Add a JavaScript
After making a rectangular shape using canvas tag , you must A JS to make drawing . look ate the following example that made a stight line drawing inside the rectangle

```
<!DOCTYPE html>
<html>
<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #d3d3d3;">
Your browser does not support the HTML canvas tag.</canvas>

<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0,0);
ctx.lineTo(200,100);
ctx.stroke();
</script>

</body>
</html>

```












and the result will be like this
<!DOCTYPE html>
<html>
<body>

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #d3d3d3;">
Your browser does not support the HTML canvas tag.</canvas>

<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0,0);
ctx.lineTo(200,100);
ctx.stroke();
</script>

</body>
</html>

&nbsp;


### Note that there are alot of drawings you can make by using JS such as circle , text ,image or even drawing a linear gradient.
