# SENDING FORM DATA

- The web runs on a client/server architecture, which can be summarized as follows. The HTTP protocol is used by a client to send a message to a server. The same protocol is used by the server to respond to the message.

- A web page's HTML type is nothing more than a user-friendly way to set up an HTTP request to transfer data to a server. This requires the user to include details that would be used in the HTTP search.

- On the client side, you'll need to find out how to send the info. The variable determines the format in which the data will be sent. Its attributes are all designed to allow you to modify the request that is submitted when a user clicks the submit button. Action and process are the two most important characteristics.

- The action attribute is used to explain how something is done. Where the data is sent is calculated by the action attribute. It must have a legitimate relative or absolute URL as its value. If this attribute isn't defined, the data would be submitted to the current page's URL, which is the URL of the page that includes the form.









### Form Attributes 


1-```action = "url"``` : the data will be sent to the specified url / if none to the same page.

2-```method = "GET" ```: the data will be sent as a request in the header. (url/?key=value&key2=value2).

3-```method = "POST" ```: the data will be sent as a request in the body. (more secure, better for longer data, and sending files).

## Form tag attributes 

- action = "/path-to-url"

- method = "GET/POST"

- name = "formName"

- autocomplete = "on/off"

- target = "_blank" (new tab) / "_self" (current tab)

- enctype = "text/plain" (text input form) "multipart/form-data" (forms containing files)