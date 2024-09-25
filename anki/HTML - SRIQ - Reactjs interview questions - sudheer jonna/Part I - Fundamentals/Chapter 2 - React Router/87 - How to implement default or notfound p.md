========== Question ==========  

### How to implement _default_ or _NotFound_ page?  

========== Answer ==========  

A `<Switch>` renders the first child `<Route>` that matches. A `<Route>` with no path always matches. So you just need to simply drop path attribute as below

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">Switch</span>>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> <span class="hljs-attr">exact</span> <span class="hljs-attr">path</span>=<span class="hljs-string">'/'</span> <span class="hljs-attr">component</span>=<span class="hljs-string">{Home}</span> /></span></span>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> <span class="hljs-attr">path</span>=<span class="hljs-string">'/user'</span> <span class="hljs-attr">component</span>=<span class="hljs-string">{User}</span> /></span></span>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> <span class="hljs-attr">component</span>=<span class="hljs-string">{NotFound}</span> /></span></span>
&#x3C;/<span class="hljs-title class_">Switch</span>>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
87

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#87-How-to-implement-default-or-notfound-p

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
