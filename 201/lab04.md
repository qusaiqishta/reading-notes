# links
either if you want to build a website contains more than one page or you want to link your website with an external websites , you have to use something called *link tag* (a) this tage allow you to link your website pages to each other and also put an external link inside your website.
#### worth to mention that an (a) tag has an attribute called (href) which is contain the resource of the link. for example if you want to add a link of an external website , you have to copy the absolute URL of that website , but if you want to connet one page to another in the same website you have to copy the relatice path or relative URL of one page and paste it in href attribute in another page.

Note that you can make you email address as a link in your website by using (mailto) tag. look at the following example

``` <a href="mailto:jon@example.org">Email Jon</a>```

Note that By default, the linked page will be displayed in the current browser window. To change this, you must specify another target for the link.
for example if you want the link to open in another you should specify the target to (_blank) .

in case you want to know more about links [check this link](https://www.w3schools.com/html/html_links.asp)

&nbsp;


# Layout
CSS allow the designer to control and change the layout of the webpage as long as he want. As you know that CSS treat evey part of the HTML page as it surrounded by a box , from here you have to imagine that every part of your web page included in it's own box , then you can to change the characteristics of that box as you want.For example, you can specify the position of each box(part) inside the window for instance you can make a paragraphs follow something called **Normal flow** in which they appear one
after the other, vertically down
the page. or even you can make their postions relative to each other (Relative Positioning)
or you can make some parts of the page content float in which the remaining content will be around it.
 #### Note that When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. to solve this problem use (z-index). . Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5.

 &nbsp;

# screen size
There is no doubt that the individual users differs from each other in terms of the devices they use to open your website , therfore the size of the page content that you already specified may be changed according to the size of window that the user used.
There are mainly two methods to solve this problem:

1-**Fixed width layout**: in which
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels. But this methodmay end up with big gaps
around the edge of a page if the user screen is bigger than your's.

2-**Liquid layout** in which designs
stretch and contract
as the user increases
or decreases the
size of their browser
window. They tend to
use percentages.But this method has some disadvantages such as If the user has a wide
window, lines of text can
become very long, which
makes them harder to read.

# What is a Function and why we use it inside a HTML code?
Functions let you group a series of statements together to perform a
specific task. If different parts of a script repeat the same task, you can
reuse the function (rather than repeating the same set of statements)

# How functions work?
1-The program comes to a line of code containing a "function call".

2-The program enters the function (starts at the first line in the function code).

3-All instructions inside of the function are executed from top to bottom.

4-The program leaves the function and goes back to where it started from.

5-Any data computed and RETURNED by the function is used in place of the function in the original line of code.

# function syntex
**function** functionName()
{
    excuted statements;
}

### Note that we can use array inside a function in order to return more than one value.Look at the following example


function getSize (width, height, depth) 

{
var area = width * height;

var volume = width * height * depth;

var sizes= [area , volume];

return sizes;

var areaOne = getSize (3, 2, 3)[0]; *used index zero to return the area*

var volumeOne = getSize (3, 2, 3)[1]; *used index one to return the volume*

&nbsp;

# pair programming

pair programming is simply means two persons working on the same code or project , one of them called driver which is the programmer that responsible for coding stuff and the other called navigator which responible for directing , monitoring , transforming algorithm into written code and helping the director to focus on the big picture.
This working strategy has many benefits such as it will inhance the social and technical skills for both programmers also it will improve the quality of results in which when two persons working togother the ability to generate more ideas and reducing errors significantly increase which lead to improve quality.

 


