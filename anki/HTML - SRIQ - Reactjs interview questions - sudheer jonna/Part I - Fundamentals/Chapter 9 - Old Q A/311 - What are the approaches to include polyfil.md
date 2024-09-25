========== Question ==========  

### What are the approaches to include polyfills in your `create-react-app`?  

========== Answer ==========  

There are approaches to include polyfills in create-react-app,

1.  **Manual import from `core-js`:**

    Create a file called (something like) `polyfills.js` and import it into root `index.js` file. Run `npm install core-js` or `yarn add core-js` and import your specific required features.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> <span class="hljs-string">'core-js/fn/array/find'</span>;
        <span class="hljs-keyword">import</span> <span class="hljs-string">'core-js/fn/array/includes'</span>;
        <span class="hljs-keyword">import</span> <span class="hljs-string">'core-js/fn/number/is-nan'</span>;
        </code></pre>
    <!-- codeblock-end -->

2.  **Using Polyfill service:**

    Use the polyfill.io CDN to retrieve custom, browser-specific polyfills by adding this line to `index.html`:

    <!-- codeblock-start -->
    <pre><code class="hljs language-html">
        <span class="hljs-tag">&#x3C;<span class="hljs-name">script</span> <span class="hljs-attr">src</span>=<span class="hljs-string">"https://cdn.polyfill.io/v2/polyfill.min.js?features=default,Array.prototype.includes"</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">script</span>></span>
        </code></pre>
    <!-- codeblock-end -->

    In the above script we had to explicitly request the `Array.prototype.includes` feature as it is not included in the default feature set.

========== Id ==========  
311

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#311-What-are-the-approaches-to-include-polyfil

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
