# Web Scraping

Web scraping is an automated method used to extract large amounts of data from websites. The data on the websites are unstructured. Web scraping helps collect these unstructured data and store it in a structured form. There are different ways to scrape websites such as online Services, APIs or writing your own code. In this article, we’ll see how to implement web scraping with python. 




## Why is Web Scraping Used?
Web scraping is used to collect large information from websites. But why does someone have to collect such large data from websites? To know about this, let’s look at the applications of web scraping:

- Price Comparison: Services such as ParseHub use web scraping to collect data from online shopping websites and use it to compare the prices of products.

- Email address gathering: Many companies that use email as a medium for marketing, use web scraping to collect email ID and then send bulk emails.

- Social Media Scraping: Web scraping is used to collect data from Social Media websites such as Twitter to find out what’s trending.

- Research and Development: Web scraping is used to collect a large set of data (Statistics, General Information, Temperature, etc.) from websites, which are analyzed and used to carry out Surveys or for R&D.

- Job listings: Details regarding job openings, interviews are collected from different websites and then listed in one place so that it is easily accessible to the user.

## Web Scraping Steps

- Step 1: Find the URL that you want to scrape

- Step 2: Inspecting the Page

The data is usually nested in tags. So, we inspect the page to see, under which tag the data we want to scrape is nested

- Step 3: Find the data you want to extract


- Step 4: Write the code


### Is Web Scraping Legal?

Talking about whether web scraping is legal or not, some websites allow web scraping and some don’t. To know whether a website allows web scraping or not, you can look at the website’s “robots.txt” file. You can find this file by appending “/robots.txt” to the URL that you want to scrape.


## What is a beautiful soup

Beautiful Soup is a Python package for parsing HTML and XML documents (including having malformed markup, i.e. non-closed tags, so named after tag soup). It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for web scraping