# Forms 
A term form refers simply refer to document that has space which llow the user to inpud data in it. the most common example of a form is the search bar that contained in Google.com in which allow the user to input different type of data and search for a specific subjects.


### There are different types of forms control :
- **Adding text:**

1- Text input: allow user to input single line text.

2- Password input: allow user to input single line of both text and charecters.

3- Text area: to input multible lines of text.


- **Making choices**:

1- Radio buttons: to select one option from number of options

2- Checkbox: to select on or more than one option.

3- drop down box: to select one option from drop down list.

- **Submitting forms**

submit button allow the user to click on it after he add all the the above inputs

- **uploading files**: such as photos and pdf files.


&nbsp;


### How forms work:

1- the user input a data inside the forms control.

2- the data send directly to the server.

3- the server processing the data using one of the programming language then store it in a database.

4- The server creates a new
page to send back to the
browser based on the
information received.


&nbsp;

## Form syntex

- to create a form use (form) tag.

- every form tag should contain (action) attribute which contain the URL of a page inside the server to save the user input data into it.

- (method) attribute which specify the way that the data will be sent to the server and there are two ways:

 1-get method :With the get method, the values
from the form are added to
the end of the URL specified in
the action attribute.

2- post method: With the post method the
values are sent in what are
known as HTTP headers


&nbsp;

# some form elements:
- input element: The (input) element is used
to create several different form
controls

Look at the following example :
```
<form action="http://www.example.com/login.php">
<p>Username:
 <input type="text" name="username" size="15"
 maxlength="30" />
</p>
</form>
```

the example above will create form called *username*, allow user to input text with maximum charecter of 30 and the size of the form itself will be 15 . look at the result 

<form action="http://www.example.com/login.php">
<p>Username:
 <input type="text" name="username" size="15"
 maxlength="30" />
</p>
</form>

&nbsp;

- Text area element: The (textarea) element
is used to create a mutli-line
text input.

Look at the following example that make a from allow user to input multible line .
```
<form action="http://www.example.com/comments.php">
<p>What did you think of this gig?</p>
 <textarea name="comments" cols="20" rows="4">Enter
 your comments...</textarea>
</form>
```

Note that the cols attribute specify the nymber of coloumns the user can write vertically and rows attribute specify the width of the form.

The result will be like this .

<form action="http://www.example.com/comments.php">
<p>What did you think of this gig?</p>
 <textarea name="comments" cols="20" rows="4">Enter
 your comments...</textarea>
</form>

&nbsp;

# list-style-type:

The list-style-type property
allows you to control the shape
or style of a bullet point (also
known as a marker).

- it can be used to change marker that comes with an unordered list items . for example you can change it to a decimal leading zero style or to letters or even to image.

- Note that you can position the marker by using the list-style-position either outside or inside to the text box.

&nbsp;

# Tables properties:

Here are some properties that it can used to arrange the table:

- width to set the width of the
table
- padding to set the space
between the border of each table
cell and its content
- text-transform to convert the
content of the table headers to
uppercase
- letter-spacing, font-size
to add additional styling to the
content of the table headers
- border-top, border-bottom
to set borders above and below
the table headers
- text-align to align the writing
to the left of some table cells and
to the right of the others
- background-color to change
the background color of the
alternating table rows
- :hover to highlight a table row
when a user's mouse goes over it

- show : to show the border of any empty cell 

- hide: to hide the border of any empty cell.


&nbsp;

 
# HTML Events

 HTML events are "things" that happen to HTML elements. An HTML event can be something the browser does, or something a user does. For Example the clickg by user on a button or when the web page finish loading these considerd events.Look at the following example.
```
 <button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
 ```

 The botton *the time is* is condnsidered an event when the user click on it , after clicking the code will run the current time will apear.
















