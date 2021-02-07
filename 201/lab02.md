# HTML SEMANTIC ELEMENTS
As we have learned before that HTML elements are used to describe the structure of
the page (e.g. headings, subheadings, paragraphs)
but the new thing that these elements could have something called **semantic markup elements** in which these elements  are not intended to affect the
structure of your web pages, but they do add extra information to the pages
&nbsp;
### Examples of using MARKUP :
- **strong**:
The use of the strong
element indicates that its
content has strong importance.
For example, the words
contained in this element might
be said with strong emphasis.
By default, browsers will show
the contents of a strong
element in bold(Note that the using of strong and b tag will give you the same result
)
- **em** :The em element indicates
emphasis that subtly changes
the meaning of a sentence.
By default browsers will show
the contents of an em element
in italic.(Note that the use of em and i tags will give you the same result)
- **Address**:The address element has
quite a specific use: to contain
contact details for the author of
the page.
It can contain a physical address,
but it does not have to. For
example, it may also contain a
phone number or email address.

### There are a lot of semantic markup that can use to make your website meaningful. To know more about it you can check this website[w3school](https://www.w3schools.com/html/html5_semantic_elements.asp)

&nbsp;


# Why using CSS is important when launching a website
CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that
the background of the page is cream, all paragraphs should appear in gray using the Arial typeface, or that all level one
headings should be in a blue, italic, Times typeface.
# What CSS allows you to do with your HTML page?
- Boxes:
Width and height
Borders (color, width, and style)
Background color and images
Position in the browser window.
-Text:
Typeface
Size
Color
Italics, bold, uppercase,
lowercase, small-caps
- Specific:
There are also specific ways
in which you can style certain
elements such as lists, tables,
and forms.

# CSS syntex
- look at the image below to see the basic CSS syntex
![CSS](https://th.bing.com/th/id/Rd7af26d69fc0a56e8b0d6b2d1da03118?rik=yKX5L9UuxR42Xw&riu=http%3a%2f%2fgdiboston.com%2fgdi-core-html-css%2fimg%2fcss-syntax.png&ehk=3lwlTMtgWXCDCNhB9pku5CoFuCddCclNU6fjXE4Wsag%3d&risl=&pid=ImgRaw)

# There are two ways to link CSS file with the HTML file:
- **first:Using External CSS**
The <link> element can be used
in an HTML document to tell the
browser where to find the CSS
file used to style the page. It is an
empty element (meaning it does
not need a closing tag), and it
lives inside the <head> element.
It should use three attributes:
*advantages of using external CSS file summerized by:
 - Allows all pages to use the
same style rules (rather than
repeating them in each page).
- Keeps the content separate
from how the page looks.
- Means you can change the
styles used across all pages
by altering just one file
(rather than each individual
page).
- **second:Using Internal CSS**

You can also include CSS rules
within an HTML page by placing
them inside a style element,
which usually sits inside the
head element of the page.

### How Css Rules Cascade?
If there are two or more rules
that apply to the same element,
it is important to understand
which will take precedence.

1-LAST RULE

If the two selectors are identical,
the latter of the two will take
precedence. Here you can see
the second i selector takes
precedence over the first

2-SPECIFICITY

If one selector is more specific
than the others, the more
specific rule will take precedence
over more general ones. In this
example:
h1 is more specific than *
p b is more specific than p
p#intro is more specific than p

3-IMPORTANT
You can add !important after
any property value to indicate
that it should be considered
more important than other rules
that apply to the same element.   

   &nbsp;


# variables in JS
using variables is mainly for assigning values to other things in order to use it more than one time. Foe example if you want to calculate a rectangular area youar have to declare three variables which are width , lengh and area . and you have to make the area variable equal to width * lenth 
so when the user enter values for width and length varibales he will immedietly get the rectangualr area.
 #### note that: you have to use the (=) value to give the variable a value and you have to use (var or let) word in order to declare that variable
 #### There are mainly three types of data could be stored in variables which are numbers(whether integer or fractional numbers ) , strings(letters) and boolean(true or false)

 #### The main difference between using var and let is that var allow you to change the value of the variable later in the code but let do not allow you.

 #### you can store more than one value in one variable by using something called Array
 Arrays are especially helpful
when you do not know how
many items a list will contain
because, when you create the
array, you do not need to specify
how many values it will hold

   &nbsp;

# Evaluating conditions and conditional statement
A conditional statement evaluates an expression and executes instructions depending on the outcome of the evaluation. Conditionals depend on operators to evaluate if an expression is true or false. A condition and selection are not the same thing. A condition asks a question. A selection processes the answer.
Look at the following image to understand how the conditional statement work 
![image](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/If-Then-Else-diagram.svg/1920px-If-Then-Else-diagram.svg.png)
Lets take a simple example of how exactly it is work
**this file helps us to understand conditionals in Python.**
**what do you think the output will be when you execute these instructions?**

a = 5
b = "bar"

if a == 5:
    print("Yes, the variable a has been assigned to the value 5.")
else:
    print("No, the variable a has not been assigned to the value 5.")

 **what do you think the output will be when you execute these instructions?**

a = 5
b = "bar"

if b == "foo":
     print("yes, the variable b has been assigned the value foo")
else:
     print("no, the variable b has been assigned to some other value than foo.")








