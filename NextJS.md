Atomic Design 
Atomic design is a methodology for designing and building user interfaces in a systematic, reusable, and structured way.
The idea is to break down the complex user interfaces into smaller, more manageable parts or building blocks.

 

Atoms – Atoms are the smallest building blocks representing UI elements like buttons, inputs, and labels.
Molecule - Molecules are groups of atoms that work together to form more complex UI elements like forms, search bars, and product cards.
Organisms - Organisms are groups of molecules and atoms that make up entire UI components, such as headers, footers, and navigation bars.
Templates - Templates are a higher level of abstraction that defines the layout and structure of a page or interface.
Pages - Pages represent specific instances of templates with real content and data.

The atomic system creates consistency
The key idea behind atomic design is that these building blocks can be combined and reused in various combinations to create consistent and scalable user interfaces. Using atomic design, designers and developers can create a more efficient and cohesive design process by building reusable components that can be used across multiple projects.
This leads to
•	Faster development times
•	Easier maintenance
•	A more consistent user experience















Next.js
Next JS –
Next.js is a React framework for building full-stack web applications. you use React Components to build user interfaces, and Next.js for additional features and optimizations.
Under the hood, Next.js also abstracts and automatically configures tooling needed for React, like bundling, compiling, and more. This allows you to focus on building your application instead of spending time with configuration.
Whether you're an individual developer or part of a larger team, Next.js can help you build interactive, dynamic, and fast React applications.
There's no need to install additional packages. Next.js provides everything for you
React - 
Not quite possible to build a full feature rich application ready to be deployed for production React is a library for building user interfaces
You have to make decisions on other features of the app like routing, styling, authentication etc.
Stable release -	14.0.4 / 7 December 2023
Previous version - 	13.4.7 developed by Vercel (26/06/23)
Next.JS Features –
Next.js simplifies the process of building a react application of production.
1.	File based routing.
2.	Pre-rendering.
3.	API routes.
4.	Support for CSS modules.
5.	Authentication
6.	Dev and Prod build system (Built-in Optimization).
7.	Server-Side rendering.
8.	Static site generation
App Router vs Pages Router -
Next.js has two different routers: the App Router and the Pages Router. The App Router is a newer router that allows you to use React's latest features, such as Server Components and Streaming. The Pages Router is the original Next.js router, which allowed you to build server-rendered React applications and continues to be supported for older Next.js applications.
Installation-
System Requirements:
Node.js 18.17 or later.
macOS, Windows (including WSL), and Linux are supported.
Commands –
npx create-react-app my-app
npx create-next-app@latest <projectName>
# or
yarn create next-app <projectName>
# or
pnpm create next-app <projectName>
If you want to start with a TypeScript project you can use the --typescript flag:
npx create-next-app@latest –typescript <projectName>
# or
yarn create next-app –-typescript <projectName>
# or
pnpm create next-app –-typescript <projectName>
App router -
Create an app/ folder, then add a layout.tsx and page.tsx file. These will be rendered when the user visits the root of your application (/).
 
Create a root layout inside app/layout.tsx with the required <html> and <body> tags:
app/layout.tsx
export default function RootLayout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  )
}
Finally, create a home page app/page.tsx with some initial content:
app/page.tsx
export default function Page() {
  return <h1>Hello, Next.js!</h1>
}
Good to know: If you forget to create layout.tsx, Next.js will automatically create this file when running the development server with next dev.
Page Router –
If you prefer to use the Pages Router instead of the App Router, you can create a pages/ directory at the root of your project.
Then, add an index.tsx file inside your pages folder. This will be your home page (/):
pages/index.tsx
export default function Page() {
  return <h1>Hello, Next.js!</h1>
}
Next, add an _app.tsx file inside pages/ to define the global layout. Learn more about the custom App file.
pages/_app.tsx
import type { AppProps } from 'next/app'
export default function App({ Component, pageProps }: AppProps) {
  return <Component {...pageProps} />
}
Finally, add a _document.tsx file inside pages/ to control the initial response from the server. Learn more about the custom Document file.
pages/_document.tsx
import { Html, Head, Main, NextScript } from 'next/document'
export default function Document() {
  return (
    <Html>
      <Head />
      <body>
        <Main />
        <NextScript />
      </body>
    </Html>
  )
}
Local host url for nextjs - http://localhost:3000
The public folder (optional)
Create a public folder to store static assets such as images, fonts, etc. Files inside public directory can then be referenced by your code starting from the base URL (/).

Page Router - 
The Pages Router has a file-system based router built on concepts of pages. When a file is added to the page directory it's automatically available as a route. Each page is associated with a route based on its file name.
Routing Section intro –
Routing in a React.js app
•	Install a third-party package.
•	routes.js file to configure the routes.
•	For each route, create a component file, export the component, import it in route.js and configure the new route with a path property.

Routing in a Next.js app –
•	File-system based routing mechanism.
•	When a file is added to the pages folder in a project, it automatically become available as a route.
•	By mixing and matching file names with a nested folder structure, it is possible to pretty much define the most common routing patterns.

Steps –
Route with pages.
Nested routes.
Dynamic routes.
Catch-all-routes.
	Navigate from the UI.
	Programmatically navigate b/w pages.

Scenario 1 : http://localhost:3000   --Home Page  --- initial Route for app
Scenario 2 : http://localhost:3000/about --About Page --- route with pages
Scenario 3 : http://localhost:3000/blog --Blog Page, http://localhost:3000/blog/firstblog -- FirstBlog Page ---nested routes
Scenario 4 : http://localhost:3000/product/1 -- Product 1 details  ---dynamic routes
Scenario 5 : http://localhost:3000/product/1/review/1 -- Product review 1 details --dynamic routes
Scenario 6 : http://localhost:3000/docs/feature1/concept1 ---Catch all routes
                      http://localhost:3000/docs/feature1/concept2
                      http://localhost:3000/docs/feature2/concept5
                      http://localhost:3000/docs/feature5/concepte4

Index routes
The router will automatically route files named index to the root of the directory.
pages/index.js → /
pages/blog/index.js → /blog
Nested routes
The router supports nested files. If you create a nested folder structure, files will automatically be routed in the same way still.
pages/blog/first-post.js → /blog/first-post
pages/dashboard/settings/username.js → /dashboard/settings/username
Layout Pattern
The React model allows us to deconstruct a page into a series of components. Many of these components are often reused between pages.
For example, you might have the same navigation bar and footer on every page.
Single Shared Layout with Custom App
import Layout from '../components/layout'
export default function MyApp({ Component, pageProps }) {
  return (
	<Navbar />
      <main> <Component {...pageProps} /></main>
      <Footer />
  )
}
Per-Page Layouts
If you need multiple layouts, you can add a property getLayout to your page, allowing you to return a React component for the layout. This allows you to define the layout on a per-page basis. Since we're returning a function, we can have complex nested layouts if desired.
Data Fetching
Inside your layout, you can fetch data on the client-side using useEffect or a library like SWR. Because this file is not a Page, you cannot use getStaticProps or getServerSideProps currently.
import useSWR from 'swr'
import Navbar from './navbar'
import Footer from './footer'
export default function Layout({ children }) {
  const { data, error } = useSWR('/api/navigation', fetcher)
  if (error) return <div>Failed to load</div>
  if (!data) return <div>Loading...</div>
 return (
    <>
      <Navbar links={data.links} />
      <main>{children}</main>
      <Footer />
    </>
  )
}
Dynamic Routes
When you don't know the exact segment names ahead of time and want to create routes from dynamic data, you can use Dynamic Segments that are filled in at request time or prerendered at build time.
Convention
A Dynamic Segment can be created by wrapping a file or folder name in square brackets: [segmentName]. For example, [id] or [slug].
Dynamic Segments can be accessed from useRouter.
Example
For example, a blog could include the following route pages/blog/[slug].js where [slug] is the Dynamic Segment for blog posts.
import { useRouter } from 'next/router'
export default function Page() {
  const router = useRouter()
  return <p>Post: {router.query.slug}</p>
}
Route	Example URL	params
pages/blog/[slug].js	/blog/a	{slug: 'a’}
pages/blog/[slug].js	/blog/b	{slug: 'b’}
pages/blog/[slug].js	/blog/c		{slug: 'c’}
Catch-all Segments
Dynamic Segments can be extended to catch-all subsequent segments by adding an ellipsis inside the brackets [...segmentName].
For example, pages/shop/[...slug].js will match /shop/clothes, but also /shop/clothes/tops, /shop/clothes/tops/t-shirts, and so on.
Route	Example URL	params
pages/shop/[...slug].js	/shop/a	{ slug: ['a'] }
pages/shop/[...slug].js	/shop/a/b	{ slug: ['a', 'b'] }
pages/shop/[...slug].js	/shop/a/b/c	{ slug: ['a', 'b', 'c'] }

Optional Catch-all Segments
Catch-all Segments can be made optional by including the parameter in double square brackets: [[...segmentName]].
For example, pages/shop/[[...slug]].js will also match /shop, in addition to /shop/clothes, /shop/clothes/tops, /shop/clothes/tops/t-shirts.
The difference between catch-all and optional catch-all segments is that with optional, the route without the parameter is also matched (/shop in the example above).
Route	Example URL	params
pages/shop/[[...slug]].js	/shop		{ slug: [] }
pages/shop/[[...slug]].js	/shop/a	{ slug: ['a'] }
pages/shop/[[...slug]].js	/shop/a/b	{ slug: ['a', 'b'] }
pages/shop/[[...slug]].js	/shop/a/b/c	{ slug: ['a', 'b', 'c'] }
Link Component
When linking between pages on websites, you use the <a> HTML tag.
In Next.js, you can use the Link Component next/link to link between pages in your application. <Link> allows you to do client-side navigation and accepts props that give you better control over the navigation behavior.
If you want external page routing use <a> tag.
Link Pre-fetching
Any <Link /> in the viewport (initially or through scroll) will be prefetched by default (including the corresponding data) for pages using Static Generation. The corresponding data for server-rendered routes is fetched only when the <Link /> is clicked.
Linking to dynamic paths
You can also use interpolation to create the path, which comes in handy for dynamic route segments. 
import Link from 'next/link'
function Posts({ posts }) {
  return (
    <ul>
      {posts.map((post) => (
        <li key={post.id}>
          <Link href={`/blog/${encodeURIComponent(post.slug)}`}>
            {post.title}
          </Link>
        </li>
      ))}
    </ul>
  )
}
export default Posts
encodeURIComponent is used in the example to keep the path utf-8 compatible.
encodeURIComponent is a JavaScript function that is used to encode a URI component. In other words, it takes a string as input and returns a new string in which certain characters that have a special meaning in a URI are replaced with their corresponding percent-encoded values.
For example, characters such as spaces, ampersands, and question marks are not allowed in certain parts of a URI, and using encodeURIComponent ensures that these characters are properly encoded so that they don't interfere with the structure of the URI.
var originalString = "Hello, World!";
var encodedString = encodeURIComponent(originalString);
console.log(encodedString);
// Output: Hello%2C%20World%21
Alternatively, using a URL Object:
import Link from 'next/link'
function Posts({ posts }) {
  return (
    <ul>
      {posts.map((post) => (
        <li key={post.id}>
          <Link
            href={{
              pathname: '/blog/[slug]',
              query: { slug: post.slug },
            }}
          >
            {post.title}
          </Link>
        </li>
      ))}
    </ul>
  )
}
export default Posts
Now, instead of using interpolation to create the path, we use a URL object in href where:
pathname is the name of the page in the pages directory. /blog/[slug] in this case.
query is an object with the dynamic segment. slug in this case.

Imperative Routing
next/link should be able to cover most of your routing needs, but you can also do client-side navigations without it, take a look at the documentation for next/router.
import { useRouter } from 'next/router'
export default function ReadMore() {
  const router = useRouter()
  return (
    <button onClick={() => router.push('/about')}>
</button>
  )
}

Shallow routing allows you to change the URL without running data fetching methods again, that includes getServerSideProps, getStaticProps, and getInitialProps.

You'll receive the updated pathname and the query via the router object (added by useRouter or withRouter), without losing state.
import { useEffect } from 'react'
import { useRouter } from 'next/router'
// Current URL is '/'
function Page() {
  const router = useRouter()
  useEffect(() => {
    // Always do navigations after the first render
    router.push('/?counter=10', undefined, { shallow: true })
  }, [])
  useEffect(() => {
    // The counter changed!
  }, [router.query.counter])
}
export default Page
404 Page
404 – NOT found, the browser was able to communicate with a given server, but the server could not find what was requested.
If you want to customize 404 error page, create 404.tsx/.js file under pages folder.
Customizing The 500 Page
500 – Internal Server Error the server encountered an unexpected condition that prevented it from fulfilling the request.
To customize the 500 page you can create a pages/500.js file. This file is statically generated at build time.
API routes -
API routes provide a solution to build a public API with Next.js.
Any file inside the folder pages/api is mapped to /api/* and will be treated as an API endpoint instead of a page. They are server-side only bundles and won't increase your client-side bundle size.
API : An application programming interface is a way for two or more computer programs or components to communicate with each other.
pages/api/hello.ts
import type { NextApiRequest, NextApiResponse } from 'next'
type ResponseData = {
  message: string
}
export default function handler(
  req: NextApiRequest,
  res: NextApiResponse<ResponseData>
) {
  if (req.method === 'POST') {
    // Process a POST request
 	res.status(200).json({ message: 'Hello from Next.js!' })
  } else {
    // Handle any other HTTP method
  }
}

Good to know:
API Routes do not specify CORS headers, meaning they are same-origin only by default. You can customize such behavior by wrapping the request handler with the CORS request helpers.

Request Helpers
API Routes provide built-in request helpers which parse the incoming request (req):
req.cookies - An object containing the cookies sent by the request. Defaults to {}
req.query - An object containing the query string. Defaults to {}
req.body - An object containing the body parsed by content-type, or null if no body was sent

Response Helpers
The Server Response object, (often abbreviated as res) includes a set of Express.js-like helper methods to improve the developer experience and increase the speed of creating new API endpoints.
The included helpers are:
res.status(code) - A function to set the status code. code must be a valid HTTP status code
res.json(body) - Sends a JSON response. body must be a serializable object
res.send(body) - Sends the HTTP response. body can be a string, an object or a Buffer
res.redirect([status,] path) - Redirects to a specified path or URL. status must be a valid HTTP status code. If not specified, status defaults to "307" "Temporary redirect".
res.revalidate(urlPath) - Revalidate a page on demand using getStaticProps. urlPath must be a string.
Dynamic API Routes
API Routes support dynamic routes, Catch all API routes, Optional catch all API routes, and follow the same file naming rules used for pages/.
pages/api/post/[pid].ts
import type { NextApiRequest, NextApiResponse } from 'next'
export default function handler(req: NextApiRequest, res: NextApiResponse) {
  const { pid } = req.query
  res.end(`Post: ${pid}`)
}
Routing Summary
1. Page based routing mechanism - Pages are associated with a route based on their file name 2. Nested routes - Nested folder structure, files will be automatically routed in the same way in the URL
3. Dynamic routes - Can be created by adding square brackets to a page name
4. Catch all routes - Add three dots inside square brackets to create a catch all route. Helpful when you want different URLS for the same page layout or even when you're working with pages where some of the route parameters are optional
5. Link component to navigate on click of an element
6. useRouter hook's router.push method to navigate programmatically
7. How to create a custom 404 page
Internationalization -
Next.js has built-in support for internationalized (i18n) routing since v10.0.0. You can provide a list of locales, the default locale, and domain-specific locales and Next.js will automatically handle the routing.
Locale Strategies
next.config.js
module.exports = {
  i18n: {
    locales: ['en-US', 'fr', 'nl-NL'],
    defaultLocale: 'en-US',
    domains: [
      {
        domain: 'example.com',
        defaultLocale: 'en-US',
      },
      {
        domain: 'example.nl',
        defaultLocale: 'nl-NL',
      },
      {
        domain: 'example.fr',
        defaultLocale: 'fr',
        // an optional http field can also be used to test,locale domains locally with http instead of https
        http: true,
      },
    ],
  },
}
There are two locale handling strategies: Sub-path Routing and Domain Routing.
: Sub-path Routing
pages/blog.js
Domain Routing
•	example.fr/blog

Automatic Locale Detection
When a user visits the application root (generally /), Next.js will try to automatically detect which locale the user prefers based on the Accept-Language header and the current domain.
If a locale other than the default locale is detected, the user will be redirected to either:
When using Sub-path Routing: The locale prefixed path
When using Domain Routing: The domain with that locale specified as the default
When using Domain Routing, if a user with the Accept-Language header fr;q=0.9 visits example.com, they will be redirected to example.fr since that domain handles the fr locale by default.

When using Sub-path Routing, the user would be redirected to /fr.
Disabling Automatic Locale Detection
module.exports = {
  i18n: {
    localeDetection: false,
  },
}
Accessing the locale information
You can access the locale information via the Next.js router. For example, using the useRouter() hook the following properties are available:
•	locale contains the currently active locale.
•	locales contains all configured locales.
•	defaultLocale contains the configured default locale.
Transition between locales
You can use next/link or next/router to transition between locales.
import Link from 'next/link'
 
export default function IndexPage(props) {
  return (
    <Link href="/another" locale="fr">
      To /fr/another
    </Link>
  )
}
import { useRouter } from 'next/router'
 
export default function IndexPage(props) {
  const router = useRouter()
 
  return (
    <div
      onClick={() => {
        router.push('/another', '/another', { locale: 'fr' })
      }}
    >
      to /fr/another
    </div>
  )
}
const { pathname, asPath, query } = router// change just the locale and maintain all other route information including href's queryrouter.push({ pathname, query }, asPath, { locale: nextLocale })
import Link from 'next/link'
 
export default function IndexPage(props) {
  return (
    <Link href="/fr/another" locale={false}>
      To /fr/another
    </Link>
  )
}
Limits for the i18n config
locales: 100 total locales
domains: 100 total locale domain items
Good to know: These limits have been added initially to prevent potential performance issues at build time. You can workaround these limits with custom routing using Middleware in Next.js 12.

App Routes –
Routing Fundamentals
The skeleton of every application is routing. This page will introduce you to the fundamental concepts of routing for the web and how to handle routing in Next.js.
Terminology
Tree: A convention for visualizing a hierarchical structure.
Subtree: Part of a tree, starting at a new root (first) and ending at the leaves (last).
Root: The first node in a tree or subtree, such as a root layout.
Leaf: Nodes in a subtree that have no children, such as the last segment in a URL path.
URL Segment: Part of the URL path delimited by slashes.
URL Path: Part of the URL that comes after the domain (composed of segments).
The App Router works in a new directory named app. The app directory works alongside the pages directory to allow for incremental adoption. This allows you to opt some routes of your application into the new behavior while keeping other routes in the pages directory for previous behavior.
Good to know: The App Router takes priority over the Pages Router. Routes across directories should not resolve to the same URL path and will cause a build-time error to prevent a conflict.
Pages
A page is UI that is unique to a route. You can define pages by exporting a component from a page.js file. Use nested folders to define a route and a page.js file to make the route publicly accessible.
Good to know:
A page is always the leaf of the route subtree.
.js, .jsx, or .tsx file extensions can be used for Pages.
A page.js file is required to make a route segment publicly accessible.
Pages are Server Components by default but can be set to a Client Component.
Pages can fetch data.
In this example, the /dashboard/analytics URL path is not publicly accessible because it does not have a corresponding page.js file. This folder could be used to store components, stylesheets, images, or other colocated files.
 
Advanced Routing Patterns
The App Router also provides a set of conventions to help you implement more advanced routing patterns. These include:
Parallel Routes: Allow you to simultaneously show two or more pages in the same view that can be navigated independently. You can use them for split views that have their own sub-navigation. E.g. Dashboards.
Intercepting Routes: Allow you to intercept a route and show it in the context of another route. You can use these when keeping the context for the current page is important. E.g. Seeing all tasks while editing one task or expanding a photo in a feed.
These patterns allow you to build richer and more complex UIs, democratizing features that were historically complex for small teams and individual developers to implement.
Layouts
A layout is UI that is shared between multiple pages. On navigation, layouts preserve state, remain interactive, and do not re-render. Layouts can also be nested.
You can define a layout by default exporting a React component from a layout.js file. The component should accept a children prop that will be populated with a child layout (if it exists) or a child page during rendering.
app/dashboard/layout.tsx
export default function DashboardLayout({
  children, // will be a page or nested layout
}: {
  children: React.ReactNode
}) {
  return (
    <section>
      {/* Include shared UI here e.g. a header or sidebar */}
      <nav></nav>
 
      {children}
    </section>
  )
}
Good to know:
The top-most layout is called the Root Layout. This required layout is shared across all pages in an application. Root layouts must contain html and body tags.
Any route segment can optionally define its own Layout. These layouts will be shared across all pages in that segment.
Layouts in a route are nested by default. Each parent layout wraps child layouts below it using the React children prop.
You can use Route Groups to opt specific route segments in and out of shared layouts.
Layouts are Server Components by default but can be set to a Client Component.
Layouts can fetch data. View the Data Fetching section for more information.
Passing data between a parent layout and its children is not possible. However, you can fetch the same data in a route more than once, and React will automatically dedupe the requests without affecting performance.
Layouts do not have access to the route segments below itself. To access all route segments, you can use useSelectedLayoutSegment or useSelectedLayoutSegments in a Client Component.
.js, .jsx, or .tsx file extensions can be used for Layouts.
A layout.js and page.js file can be defined in the same folder. The layout will wrap the page.


Root Layout (Required)
The root layout is defined at the top level of the app directory and applies to all routes. This layout enables you to modify the initial HTML returned from the server.
app/layout.tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  )
}
Good to know:
The app directory must include a root layout.
The root layout must define <html> and <body> tags since Next.js does not automatically create them.
You can use the built-in SEO support to manage <head> HTML elements, for example, the <title> element.
You can use route groups to create multiple root layouts. See an example here.
The root layout is a Server Component by default and can not be set to a Client Component.
Nesting Layouts
Layouts defined inside a folder (e.g. app/dashboard/layout.js) apply to specific route segments (e.g. acme.com/dashboard) and render when those segments are active. By default, layouts in the file hierarchy are nested, which means they wrap child layouts via their children prop.
app/dashboard/layout.tsx
export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return <section>{children}</section>
}

Modifying <head>
In the app directory, you can modify the <head> HTML elements such as title and meta using the built-in SEO support.

Metadata can be defined by exporting a metadata object or generateMetadata function in a layout.js or page.js file.
app/page.tsx
import { Metadata } from 'next'
export const metadata: Metadata = {
  title: 'Next.js',
}
export default function Page() {
  return '...'
}
Good to know: You should not manually add <head> tags such as <title> and <meta> to root layouts. Instead, you should use the Metadata API which automatically handles advanced requirements such as streaming and de-duplicating <head> elements.

Injecting the router
To access the router object in a React component you can use useRouter or withRouter.
In general we recommend using useRouter.

Imperative Routing
next/link should be able to cover most of your routing needs, but you can also do client-side navigations without it, take a look at the documentation for next/router.

The following example shows how to do basic page navigations with useRouter:
import { useRouter } from 'next/router'
export default function ReadMore() {
  const router = useRouter()
 
  return (
    <button onClick={() => router.push('/about')}>
      Click here to read more
    </button>
  )
}


 

Pre-rendering –
React vs Next JS
By default, Next Js pre-renders every page in the application.

What does pre-render means?
Next JS generates HTML for each page in advance instead of having it all done by client-side JavaScript. 

 


Why pre-rendering –
1.	Pre-rendering improves performance - 
-	In a React app, you need to wait for the JS to be executed.
-	Perhaps fetch data from an external API and then render the UI.
-	There is a wait time for the user.
-	With a pre-rendered page, the HTML is already generated and loads faster.
2.	Pre-rendering helps with SEO – 
-	If you’re building a blog or an e-commerce site, SEO is a concern.
-	With a React app, if the search engine hits your page, it only sees a div tag with id equal to root.
-	If search engine hits a pre-rendered page though, all the content is present in the source code which help index that page.
-	If SEO is of concern for your app, pre-rendering is what you want.

Pre-rendering Summary –
Pre-rendering refers to the process of generating HTML with the necessary data for a page in our application.
Pre-rendering can result in better performance and SEO.


 
 

 
 
 
 
Note –
For API we used JSON Placeholder ready to use api.
If you want to expose your UI for routing mechanism create it under pages folder but if you want your UI for component level architecture use component folder.
 
 

 


GetStaticPaths -
If a page has Dynamic Routes and uses getStaticProps, it needs to define a list of paths to be statically generated.
When you export a function called getStaticPaths (Static Site Generation) from a page that uses dynamic routes, Next.js will statically pre-render all the paths specified by getStaticPaths.
fallback – fallback is mandatory to defined with getStaticPaths with values – 
-fallback: false
-fallback: true
-fallback: ‘blocking’

 
 
 
    
 
 
 
 
Note – Check npm json-server for api. Explore more
Get a full fake REST API with zero coding in less than 30 seconds (seriously)
npm install -g json-server

 
 
 
 
 

 

 

 
 
 

  
Context Parameters in getServerSideProps
https://nextjs.org/docs/pages/api-reference/functions/get-server-side-props#context-parameter
Context Parameters in getStaticProps
https://nextjs.org/docs/pages/api-reference/functions/get-static-props#context-parameter
Client-side Fetching
Client-side data fetching is useful when your page doesn't require SEO indexing, when you don't need to pre-render your data, or when the content of your pages needs to update frequently. Unlike the server-side rendering APIs, you can use client-side data fetching at the component level.
If done at the page level, the data is fetched at runtime, and the content of the page is updated as the data changes. When used at the component level, the data is fetched at the time of the component mount, and the content of the component is updated as the data changes.
It's important to note that using client-side data fetching can affect the performance of your application and the load speed of your pages. This is because the data fetching is done at the time of the component or pages mount, and the data is not cached.
Example refer – dashboard/index.tsx file in app
Client-side data fetching with SWR –
The team behind Next.js has created a React hook library for data fetching called SWR. It is highly recommended if you are fetching data on the client-side. It handles caching, revalidation, focus tracking, refetching on intervals, and more.SWR will automatically cache the data for us and will revalidate the data if it becomes stale.
Example refer – dashboard-swr.tsx file in app
Note – Learn about SWR

 
Note-refer events file for sallow routing.
 
 
 
 
 
 
Note –
npm i bootstrap
npm i sass
npm i styled-components


CSS Modules
Next.js has built-in support for CSS Modules using the .module.css extension.
CSS Modules locally scope CSS by automatically creating a unique class name. This allows you to use the same class name in different files without worrying about collisions. This behavior makes CSS Modules the ideal way to include component-level CSS.
 
Global- all other external css libraries should get include under app.tsx file to apply on all the components.
 
 
 
 
 
Note - Refer blog files for preview and publish data.

 
App Layout –
Refer Header and Footer files layout in application.
Head Component –
Refer the <head> tag in index.tsx and app.tsx files.
Next Image Tag Optimization - 
The Next.js Image component extends the HTML <img> element with features for automatic image optimization:
Size Optimization: Automatically serve correctly sized images for each device, using modern image formats like WebP and AVIF.
Visual Stability: Prevent layout shift automatically when images are loading.
Faster Page Loads: Images are only loaded when they enter the viewport using native browser lazy loading, with optional blur-up placeholders.
Asset Flexibility: On-demand image resizing, even for images stored on remote servers
Note – Reference URL - https://nextjs.org/docs/pages/building-your-application/optimizing/images

Absolute Imports and Module path –
Refer the path provided in app.tsx for styles and layout.
Redirects – 
We can redirect any url to the specific url for Permanent and temporary redirect that can help us during application maintenance and old pages.
Note – Refer next.config.js file
Environment Variables –
Refer - .env.local file.
 
 
 
 
Note – Learn https://next-auth.js.org/
>npm install next-auth
Download code from https://github.com/gopinav/Next-JS-Tutorials
Auth navigation code from https://github.com/gopinav/Next-JS-Tutorials/tree/master/next-authentication








Husky –
Husky is a utility package (hook) that runs the above linting & prettier commands while committing your changes. 

