# Built-In CSS Support 

## Adding a Global Stylesheet
To add a stylesheet to your application, import the CSS file within pages/_app.js.

For example, consider the following stylesheet named styles.css:
```
body {
  font-family: 'SF Pro Text', 'SF Pro Icons', 'Helvetica Neue', 'Helvetica',
    'Arial', sans-serif;
  padding: 20px 20px 60px;
  max-width: 680px;
  margin: 0 auto;
}
```
Create a pages/_app.js file if not already present. Then, import the styles.css file.
```
import '../styles.css'

// This default export is required in a new `pages/_app.js` file.
export default function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```
These styles (styles.css) will apply to all pages and components in your application. Due to the global nature of stylesheets, and to avoid conflicts, you may only import them inside pages/_app.js.

In development, expressing stylesheets this way allows your styles to be hot reloaded as you edit them—meaning you can keep application state.

In production, all CSS files will be automatically concatenated into a single minified .css file.


## Import styles from node_modules
Since Next.js 9.5.4, importing a CSS file from node_modules is permitted anywhere in your application.

For global stylesheets, like bootstrap or nprogress, you should import the file inside pages/_app.js. For example:

// pages/_app.js
```
import 'bootstrap/dist/css/bootstrap.css'

export default function MyApp({ Component, pageProps }) {
  return <Component {...pageProps} />
}
For importing CSS required by a third party component, you can do so in your component. For example:

// components/ExampleDialog.js
import { useState } from 'react'
import { Dialog } from '@reach/dialog'
import VisuallyHidden from '@reach/visually-hidden'
import '@reach/dialog/styles.css'

function ExampleDialog(props) {
  const [showDialog, setShowDialog] = useState(false)
  const open = () => setShowDialog(true)
  const close = () => setShowDialog(false)

  return (
    <div>
      <button onClick={open}>Open Dialog</button>
      <Dialog isOpen={showDialog} onDismiss={close}>
        <button className="close-button" onClick={close}>
          <VisuallyHidden>Close</VisuallyHidden>
          <span aria-hidden>×</span>
        </button>
        <p>Hello there. I am a dialog</p>
      </Dialog>
    </div>
  )
}
```

## Sass Support
Next.js allows you to import Sass using both the .scss and .sass extensions. You can use component-level Sass via CSS Modules and the .module.scss or .module.sass extension.

Before you can use Next.js' built-in Sass support, be sure to install sass:
```
npm install sass
```
Sass support has the same benefits and restrictions as the built-in CSS support detailed above.

Note: Sass supports two different syntaxes, each with their own extension. The .scss extension requires you use the SCSS syntax, while the .sass extension requires you use the Indented Syntax ("Sass").

If you're not sure which to choose, start with the .scss extension which is a superset of CSS, and doesn't require you learn the Indented Syntax ("Sass").


## Customizing Sass Options
If you want to configure the Sass compiler you can do so by using sassOptions in next.config.js.

For example to add includePaths:
```
const path = require('path')

module.exports = {
  sassOptions: {
    includePaths: [path.join(__dirname, 'styles')],
  },
}
```


# Assets
Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.

## Download Your Profile Picture
First, let's retrieve your profile picture.

- Download your profile picture in .jpg format (or use this file).
- Create an images directory inside of the public directory.
- Save the picture as profile.jpg in the public/images directory.
- The image size can be around 400px by 400px.
- You may remove the unused SVG logo file directly under the public directory.


## Image Component and Image Optimization
next/image is an extension of the HTML <img> element, evolved for the modern web.

Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.

Automatic Image Optimization works with any image source. Even if the image is hosted by an external data source, like a CMS, it can still be optimized.

## Using the Image Component
Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.

Images are lazy loaded by default. That means your page speed isn't penalized for images outside the viewport. Images load as they are scrolled into viewport.

Images are always rendered in such a way as to avoid Cumulative Layout Shift, a Core Web Vital that Google is going to use in search ranking.

