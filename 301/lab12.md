# EJS Partials
 ### When to use 
 Partials are good to use when you have HTML element that you'll reuse across multiple views (like header, footer, navbar)


### How to use
In the files you want to use this element you add it like this:
```
<%- include( PARTIAL_FILE ) %>
```
![img](https://res.cloudinary.com/practicaldev/image/fetch/s--NcyF1ajR--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/gk1bxrwovuxzc5gnu6g7.png)

### Why use partials 
using partials makes it easier to track and modify your elements making sure they're still the same across all your pages.

