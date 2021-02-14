 # Objects 
 
Object is like a technique allow you to group number of variables and functions together in order to use them later to perform a specific task. A Variable inside an object has different name which is property and a function also has a name of method inside an object. The following example which represent the way that you can write an object using literal method.

```
 var hotel = {
name: 'Quay',
rooms: 40,
booked : 25,
checkAvailability: function() {
return this.rooms - this.booked;}}
``` 

### Some information about the previous example:
- the object has a name called (hote1) and all of it's code written inside a curly brackets.

- The object contains of number og keys( name,rooms,bookes,checkAvailability) and number of values (Quay, 40, 25, function())

- if the key is variable will called property and may hold any value of these ( nymber , boolean , string , and other..)

- if the key contains function , then will called a method and it's value will be a function.


### There are two ways to call a key from an object:
1- using dot like this. 
hote1.name  will bring a value of "Quay"

2- using square brackets like this.
hote1['name'] will bring a value of "Quay"

&nbsp;



# DOM
Document object model is simply a tree of objects the browser creat when a web page is loaded. The following picture represent the DOM tree.
![img](https://www.w3schools.com/js/pic_htmltree.gif)

With DOM , JS give you the power to change and control all the page content . For example, you can chnage the HTMl elements or attributes and also add or remove specific elements. 

### Note that every action is done on one of the HTML element is called "method" and every action done on one of the element's attribute is called "property". Look at the followig example that represnet how to change the content of one element using DOM.
```
<html>
<body>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "Hello World!";
</script>

</body>
</html>
```
in the previous example there is one method and one propert:

1- **getElementById**: it is a method used to access the HTML element( this method used id)

2-**innerHTML**: it is a property used to change the content of an element.

### Note that there are many ways to access and change the content of the web page. Here are some of them 
you can access the HTML elements by many ways like this.

| method                     | Description |
| -----------                | ----------- |
| document.getElementById(id)      | Find an element by element id       |
| document.getElementsByTagName(name)   | Find elements by tag name            | 

&nbsp;

And you can change the elements content by this properties:

| property      | Description |
| ----------- | ----------- |
| element.innerHTML =  new html content      | Change the inner HTML of an element       |
| element.attribute = new value   | Change the attribute value of an HTML element        |


 If you want to know more about methods and properties [vist](https://www.w3schools.com/js/js_htmldom_document.asp)


### Notethat before you make some changes on the element you have first to acces that element either by it's id or by it's tag name or by other method. Look at the following example.
```

<!DOCTYPE html>
<html>
<body>

<h2>Finding HTML Elements by Id</h2>

<p id="intro">Hello World!</p>
<p>This example demonstrates the <b>getElementsById</b> method.</p>

<p id="demo"></p>

<script>
var myElement = document.getElementById("intro");
document.getElementById("demo").innerHTML = 
"The text from the intro paragraph is " + myElement.innerHTML;
</script>

</body>
</html>
```

this example above access the paragraph that has id called intro and change it's content to become like this.


**The text from the intro paragraph is Hello World!**















