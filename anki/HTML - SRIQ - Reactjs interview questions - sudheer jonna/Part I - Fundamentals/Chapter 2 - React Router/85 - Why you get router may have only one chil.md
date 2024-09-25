========== Question ==========  

### Why you get "Router may have only one child element" warning?  

========== Answer ==========  

You have to wrap your Route's in a `<Switch>` block because `<Switch>` is unique in that it renders a route exclusively.

At first you need to add `Switch` to your imports:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">Switch</span>, <span class="hljs-title class_">Router</span>, <span class="hljs-title class_">Route</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router'</span>;
</code></pre>
<!-- codeblock-end -->

Then define the routes within `<Switch>` block:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">Router</span>>
  <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Switch</span>></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> {/* <span class="hljs-attr">...</span> */} /></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> {/* <span class="hljs-attr">...</span> */} /></span>
  <span class="hljs-tag">&#x3C;/<span class="hljs-name">Switch</span>></span></span>
&#x3C;/<span class="hljs-title class_">Router</span>>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
85

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#85-Why-you-get-router-may-have-only-one-chil

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
