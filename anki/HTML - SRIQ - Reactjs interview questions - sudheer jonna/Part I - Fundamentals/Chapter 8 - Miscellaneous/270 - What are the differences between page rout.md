========== Question ==========  

### What are the differences between page router and app router in nextjs?  

========== Answer ==========  

The Page Router and App Router are two different routing systems in Next.js, with the App Router being the newer and more feature-rich option. Let's compare them:

1. Structure:

    - Page Router: Uses a file-system based routing in the `pages` directory.

    - App Router: Uses a new `app` directory with a more flexible file-system based routing.

2. Rendering Model:

    - Page Router: Primarily uses client-side rendering with options for server-side rendering.

    - App Router: Defaults to server-side rendering with client-side rendering as an option.

3. Data Fetching:

    - Page Router: Uses methods like `getServerSideProps`, `getStaticProps`, and `getInitialProps`.

    - App Router: Introduces new data fetching methods within React components, supporting both client and server components.

4. Layouts:

    - Page Router: Requires manual implementation of layouts, often using Higher Order Components or custom \_app.js files.

    - App Router: Has built-in support for nested layouts using layout.js files.

5. Loading UI:

    - Page Router: Requires manual implementation of loading states.

    - App Router: Provides built-in support for loading UI with loading.js files.

6. Error Handling:

    - Page Router: Uses custom error pages (e.g., 404.js, 500.js).

    - App Router: Introduces error.js files for more granular error handling.

7. Static and Dynamic Rendering:

    - Page Router: Configured through separate functions like `getStaticProps` and `getServerSideProps`.

    - App Router: Uses a single `fetch` function with caching options to determine rendering method.

8. Middleware:

    - Page Router: Middleware applies to all routes.

    - App Router: Allows more granular middleware application, including per-route basis.

9. Route Groups:

    - Page Router: Does not have a concept of route groups.

    - App Router: Introduces route groups for better organization without affecting the URL structure.

10. Parallel Routes:

    - Page Router: Does not support parallel routes.

    - App Router: Allows rendering multiple pages in the same layout simultaneously.

Let's illustrate some of these differences with code examples:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Page Router Example</span>
<span class="hljs-comment">// pages/index.js</span>
<span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Home</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">const</span> [count, setCount] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">0</span>)
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Welcome to my app<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>Count: {count}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> setCount(count + 1)}>Increment<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
  )
}
<span class="hljs-comment">// pages/about.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">About</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>About Page<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>
}
<span class="hljs-comment">// App Router Example</span>
<span class="hljs-comment">// app/page.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Home</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Welcome to my app<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">ClientComponent</span> /></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
  )
}
<span class="hljs-comment">// app/ClientComponent.js</span>
<span class="hljs-string">'use client'</span>
<span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">ClientComponent</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">const</span> [count, setCount] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">0</span>)
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>Count: {count}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> setCount(count + 1)}>Increment<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
    <span class="hljs-tag">&#x3C;/></span></span>
  )
}
<span class="hljs-comment">// app/about/page.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">About</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>About Page<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>
}
<span class="hljs-comment">// app/layout.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">RootLayout</span>(<span class="hljs-params">{ children }</span>) {
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">html</span> <span class="hljs-attr">lang</span>=<span class="hljs-string">"en"</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">body</span>></span>{children}<span class="hljs-tag">&#x3C;/<span class="hljs-name">body</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">html</span>></span></span>
  )
}
<span class="hljs-comment">// app/loading.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Loading</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>Loading...<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span></span>
}
<span class="hljs-comment">// app/error.js</span>
<span class="hljs-string">'use client'</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Error</span>(<span class="hljs-params">{ error, reset }</span>) {
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>Something went wrong!<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> reset()}>Try again<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
  )
}
</code></pre>
<!-- codeblock-end -->

Key observations from these examples:

1. In the Page Router, all components are client-side by default. In the App Router, components are server-side by default, and we use the 'use client' directive for client-side components.

2. The App Router introduces new files like `layout.js`, `loading.js`, and `error.js` for handling common patterns.

3. The file structure in the `app` directory directly corresponds to the URL structure, similar to the `pages` directory but with more flexibility.

4. The App Router separates the layout (`layout.js`) from the page content (`page.js`), allowing for more reusable and maintainable code.

The App Router is generally recommended for new projects due to its improved performance and developer experience. However, the Page Router is still supported and may be preferred for certain use cases or when maintaining existing projects.

========== Id ==========  
270

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#270-What-are-the-differences-between-page-rout

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
