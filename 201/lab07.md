# Tables
A table is something used to arrange data in rows and columns.Look at the following example to see how we make a table inside HTML.

```
<table>
 <tr>
 <td>15</td>
 <td>15</td>
 <td>30</td>
 </tr>
 <tr>
 <td>45</td>
 <td>60</td>
 <td>45</td>
 </tr>
 <tr>
 <td>60</td>
 <td>90</td>
 <td>90</td>
 </tr>
</table>
```
### Information about the previous example:
- we use *table* tage to make a table.

- we use *tr* tage to indicate the start of a row .

- we use *td* tag to assign a value for each cell in a row.
- the result of the example will be like this:

15 15 30

45 60 45

60 90 60

### Note that you can use the *th* tag instead of *td* tag to assign a value to each cell and to represent a heading for either a row or column.

### NOte that if you want to specify the number of coloumns , you should use *colspan* attribute inside *td* or *th* tag.

### Note that you can add some features to the table content to make it looks nice. For example you can add a border , specify margin , padding , texg-align and many other.

 &nbsp;

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

## There is another way to make an object which is called CONSTRUCTOR SYNTAX:
```


var hotel = new Object();
hotel.name= 'Park';
hotel.rooms = 120;
hotel .booked = 77;
hotel .checkAvailability = function()
return this.rooms - this.booked;
} ; 

```

In this method you have first to define the object then assign valuse to it using the object name followed by dot then the property name.








