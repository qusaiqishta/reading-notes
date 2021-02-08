# HTML Lists
There are mainly three ways in which the list can be written in HTML:

1-**ordered lists**: in which the items will be ordered according to numbers . you can make an ordered list by using (ol) tag following with (li) tag to put the elements inside it.

2-**unordered lists**: in which the items will be unordered and indicated using bullets instead of numbers. you can make an unordered list by using (ul) tag following with (li) tag to put the elements inside it.

3-**Definition lists**: this list mainly used to define some terms.you can make a Definition list by using (di) tag included two tags. the first one is (dt) and is used to contain the term
being defined (the definition
term) , the second one is (dd) and is used to contain the definition.  
  
   &nbsp;
   
   # Using boxes
   
   as a websites maker , sometimes you have to put some boxes around some paragraphes using CSS in order to make them easier to read and more attractive. CSS provide a huge number of features that you can use to control and shape the boxes . Here are a few examples of what CSS can allow you to do with boxes:
   - **change the box dimension**: you can simply change the hight and width of the box by using *widhth* and *hight* properties and then specify the value than you want either in pixel or make it as a percentage of the window size.

   - **Limitation width and hight**:
   you can specify the maximum and minimum values for box's hight and width , so when the user open the box in either small or big window , the size of the box and conten do not change.

   - **margin**: margin means the space between a box and another one . you can specify that space by simply using the margin propert 
   - **padding**: means the space between the content inside the box and the border of the box.
   - **border**: you can also indentify the edge that surround the box by changinh it's width , color and type.

#### if you want to know more about boxes , do not hesitate to click on this [link](https://www.w3schools.com/Css/css_boxmodel.asp)

   &nbsp;

# Arrays in Javascript
An array is a special type of variable. It doesn't
just store one value; it stores a list of values.You should consider using an
array whenever you are working
with a list or a set of values that
are related to each other.
Arrays are especially helpful
when you do not know how
many items a list will contain
because, when you create the
array, you do not need to specify
how many values it will hold. this is a simple example of an array that contain three items:

var colors;

colors= ['white', 'black', ' custom'];

   &nbsp;

# switch statement
switch statement is mainly used to determine a specific value if it is match with another value or nor , in order to perform a specific block of code.Unlike if statement , switch only take a value (not expression) and look for a match of that value in it's cases on order to perform something.

#### Note that switch statement not always evaluate all the cases , once the matches value is found the switch stop in that point and does not evaluate the other cases. Look at the followin picture to see how switch exactly work.

![img](https://cdn.javascripttutorial.net/wp-content/uploads/2016/08/JavaScript-switch-case.png)


### Note that the switch statement has something called default which is has block of code evaluate if there is no case value matches the switch value.

   &nbsp;

# For loop
A for loop enables a particular set of conditions to be executed repeatedly until a condition is satisfied. Imagine a situation where you would have to print numbers from 1 to 100. What would you do? Will you type in the printf command a hundred times or try to copy/paste it? This simple task would take an eternity. Using a for loop you can perform this action in three statements. This is the most basic example of the for loop. It can also be used in many advanced scenarios depending on the problem statement. Look at the following example that try to print the numbers from 0 to 9.

for(var i=0;i<10;i++)
{
    document.write(i)
}
 
 var i=0   called initializing

 i<10     called condition or counter

 i++      called update

   &nbsp;

# while loop
The while loop loops through a block of code as long as a specified condition is true.
look at the following example to understand how while loop works 
var text = "";
var i = 0;
while (i < 10) {
  text += "<br>The number is " + i;
  i++;
}

document.write(text)

 this example result will be:

 The number is 0

The number is 1

The number is 2


The number is 3

The number is 4

The number is 5

The number is 6

The number is 7

The number is 8

The number is 9   

   &nbsp;

# Important definitions
**type coercion**: means that the JS can convert the value of the datatype in order to complete the operation .For
example, a string 'l ' could be
converted to a number 1 in the
following expression:(' 1' > 0).
As a result, the above expression
would evaluate to true. 

### *Note that the JS language called weak typing language because of coercion property.*


**truthy value**: is a value that is considered true when encountered in a Boolean context. All values are truthy unless they are defined as falsy (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN).

**Falsy value**: any thing evaluate to false such as 0, -0, 0n, "", null, undefined, and NaN.




















