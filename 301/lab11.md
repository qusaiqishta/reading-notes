# Embedded Javascript (EJS)
EJS simply stands for Embedded Javascript. It is a simple templating language/engine that lets its user generate HTML with plain javascript.

EJS is a template system. You define HTML pages in the EJS syntax and you specify where various data will go in the page. Then, your app combines data with the template and “renders” a complete HTML page where EJS takes your data and inserts it into the web page according to how you’ve defined the template. For example, you could have a table of dynamic data from a database and you want EJS to generate the table of data according to your display rules. It saves you from the drudgery of writing code to dynamically generate HTML based on data.

EJS is compatible with Express for back-end use as it hooks into the View engine architecture that Express provides and lets you render web pages to the client with res.render() in Express.

EJS (along with all the other competing template engines) allows you to generate full-blown HTML pages which certainly enables a “proper front-end”.

EJS is a tool for generating web pages that can include dynamic data and can share templated pieces with other web pages (such as common headers/footers). It is not a front-end framework. While EJS can be used by client-side Javascript to generate HTML on the client-side, it is more typically used by your back-end to generate web pages in response to some URL request. EJS is not a client-side framework like Angular or React and does not dictate what client-side framework you do or don’t use (if any). It mostly covers a separate solution space.

# Using the API:
- If the request requires authorization (such as a request for an individual's private data), then the application must provide an OAuth 2.0 token with the request. -The application may also provide the API key, but it doesn't have to.
  
- If the request doesn't require authorization (such as a request for public data), then the application must provide either the API key or an OAuth 2.0 token, or both—whatever option is most convenient for you.


- Authorizing requests with OAuth 2.0:

1- When you create your application, you register it using the Google API Console. Google then provides information you'll need later, such as a client ID and a client secret.

2-Activate the Books API in the Google API Console.

3-When your application needs access to user data, it asks Google for a particular scope of access.

4-Google displays a consent screen to the user, asking them to authorize your application to request some of their data.

5-If the user approves, then Google gives your application a short-lived access token.

6-Your application requests user data, attaching the access token to the request.

7-If Google determines that your request and the token are valid, it returns the requested data.