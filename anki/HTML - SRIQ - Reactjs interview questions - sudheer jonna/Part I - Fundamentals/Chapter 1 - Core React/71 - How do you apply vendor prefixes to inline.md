========== Question ==========  

### How do you apply vendor prefixes to inline styles in React?  

========== Answer ==========  

React _does not_ apply _vendor prefixes_ automatically. You need to add vendor prefixes manually.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;div
    style={{
        <span class="hljs-attr">transform</span>: <span class="hljs-string">'rotate(90deg)'</span>,
        <span class="hljs-title class_">WebkitTransform</span>: <span class="hljs-string">'rotate(90deg)'</span>, <span class="hljs-comment">// note the capital 'W' here</span>
        <span class="hljs-attr">msTransform</span>: <span class="hljs-string">'rotate(90deg)'</span>, <span class="hljs-comment">// 'ms' is the only lowercase vendor prefix</span>
    }}
/>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
71

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#71-How-do-you-apply-vendor-prefixes-to-inline

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
