# Pre-Rendering and Data Fetching
by default, Next.js pre-renders every page. This means that Next.js generates HTML for each page in advance, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and SEO.

Each generated HTML is associated with minimal JavaScript code necessary for that page. When a page is loaded by the browser, its JavaScript code runs and makes the page fully interactive. (This process is called hydration.)

If your app is a plain React.js app (without Next.js), there’s no pre-rendering, so you won’t be able to see the app if you disable JavaScript. For example:

Enable JavaScript in your browser and check out this page. This is a plain React.js app built with Create React App. Now, disable JavaScript and access the same page again. You won’t see the app anymore — instead, it’ll say “You need to enable JavaScript to run this app.” This is because the app is not pre-rendered into static HTML.

Two Forms of Pre-rendering:

Next.js has two forms of pre-rendering: Static Generation and Server-side Rendering. The difference is in when it generates the HTML for a page.

Static Generation is the pre-rendering method that generates the HTML at build time. The pre-rendered HTML is then reused on each request. Server-side Rendering is the pre-rendering method that generates the HTML on each request.

You can use Static Generation for many types of pages, including:

- Marketing pages
- Blog posts
- E-commerce product listings
- Help and documentation

# Dynamic Routes
we’ll talk about the case where each page path depends on external data. Next.js allows you to statically generate pages with paths that depend on external data. This enables dynamic URLs in Next.js.

How to Statically Generate Pages with Dynamic Routes In our case, we want to create dynamic routes for blog posts:

We want each post to have the path /posts/<id>, where is the name of the markdown file under the top-level posts directory. Since we have ssg-ssr.md and pre-rendering.md, we’d like the paths to be /posts/ssg-ssr and /posts/pre-rendering.














# Deploying Your Next.js App

## Push to GitHub
Before we deploy, let’s push our Next.js app to GitHub if you haven’t done so already. This will make deployment easier.

On your personal GitHub account, create a new repository called nextjs-blog.
The repository can be public or private. You do not need to initialize it with a README or other files.
If you need help setting up your repo, take a look at this guide on GitHub.
Then:

If you haven’t initialized the git repository locally for your Next.js app, do so now.
Push the Next.js app to your GitHub repository.

## Deploy to Vercel
The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database. We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. You can start using it for free — no credit card required.

## Import your nextjs-blog repository
Once you’re signed up, import your nextjs-blog repository on Vercel.

You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
Once you’ve installed Vercel, import nextjs-blog.
You can use default values for the following settings — no need to change anything. Vercel automatically detects that you have a Next.js app and chooses optimal build settings for you.

Project Name
Root Directory
Build Command
Output Directory
Development Command
When you deploy, your Next.js app will start building. It should finish in under a minute.

## Preview Deployment for Every Push
### Develop, Preview, Ship
We’ve just gone through the workflow we call DPS: Develop, Preview, and Ship.

- Develop: We’ve written code in Next.js and used the Next.js development server running to take advantage of its hot reloading feature.
- Preview: We’ve pushed changes to a branch on GitHub, and Vercel created a preview deployment that’s available via a URL. We can share this preview URL with others for feedback. In addition to doing code reviews, you can do deployment previews.
- Ship: We’ve merged the pull request to main to ship to production.