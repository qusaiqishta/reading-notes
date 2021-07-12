## how Django handles form requests 

![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)


Based on the diagram above, the main things that Django's form handling does are:

- Display the default form the first time it is requested by the user.
The form may contain blank fields (e.g. if you're creating a new record), or it may be pre-populated with initial values (e.g. if you are changing a record, or have useful default initial values).
The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).

- Receive data from a submit request and bind it to the form.
Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.

- Clean and validate the data.
Cleaning the data performs sanitization of the input (e.g. removing invalid characters that might be used to send malicious content to the server) and converts them into consistent Python types.
Validation checks that the values are appropriate for the field (e.g. are in the right date range, aren't too short or too long, etc.)

- If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.

- If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)

- Once all actions are complete, redirect the user to another page.


## Form
The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields. The class also provides methods for rendering itself in templates using predefined formats (tables, lists, etc.) or for getting the value of any element (enabling fine-grained manual rendering).

```
from django import forms

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

```

### Check [this](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms) for more fields and arguments 


## View

the view has to render the default form when it is first called and then either re-render it with error messages if the data is invalid, or process the data and redirect to a new page if the data is valid. In order to perform these different actions, the view has to be able to know whether it is being called for the first time to render the default form, or a subsequent time to validate data. 

For forms that use a POST request to submit information to the server, the most common pattern is for the view to test against the POST request type (if request.method == 'POST':) to identify form validation requests and GET (using an else condition) to identify the initial form creation request. If you want to submit your data using a GET request, then a typical approach for identifying whether this is the first or subsequent view invocation is to read the form data (e.g. to read a hidden value in the form).


## How do templates work in Django?
Django Templates. Django provides a convenient way to generate dynamic HTML pages by using its template system. A template consists of static parts of the desired HTML output as well as some special syntax describing how dynamic content will be inserted.


## How do I add a template to Django project?
To configure the Django template system, go to the settings.py file and update the DIRS to the path of the templates folder. Generally, the templates folder is created and kept in the sample directory where manage.py lives. This templates folder contains all the templates you will create in different Django Apps.


## What is a Django view?
Django views are a key component of applications built with the framework. At their simplest they are a Python function or class that takes a web request and return a web response. Views are used to do things like fetch objects from the database, modify those objects if needed, render forms, return HTML, and much more.