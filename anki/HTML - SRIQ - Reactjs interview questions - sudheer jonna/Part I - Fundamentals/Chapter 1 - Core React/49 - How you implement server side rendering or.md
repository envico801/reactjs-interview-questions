========== Question ==========  

### How you implement Server Side Rendering or SSR?  

========== Answer ==========  

React is already equipped to handle rendering on Node servers. A special version of the DOM renderer is available, which follows the same pattern as on the client side.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">ReactDOMServer</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom/server'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./App'</span>;
<span class="hljs-title class_">ReactDOMServer</span>.<span class="hljs-title function_">renderToString</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span></span>);
</code></pre>
<!-- codeblock-end -->

This method will output the regular HTML as a string, which can be then placed inside a page body as part of the server response. On the client side, React detects the pre-rendered content and seamlessly picks up where it left off.

========== Id ==========  
49

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#49-How-you-implement-server-side-rendering-or

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
