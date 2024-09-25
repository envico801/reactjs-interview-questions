========== Question ==========  

### What is route based code splitting?  

========== Answer ==========  

One of the best place to do code splitting is with routes. The entire page is going to re-render at once so users are unlikely to interact with other elements in the page at the same time. Due to this, the user experience won't be disturbed.

Let us take an example of route based website using libraries like React Router with React.lazy,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">BrowserRouter</span> <span class="hljs-keyword">as</span> <span class="hljs-title class_">Router</span>, <span class="hljs-title class_">Route</span>, <span class="hljs-title class_">Switch</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router-dom'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { <span class="hljs-title class_">Suspense</span>, lazy } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title class_">Home</span> = <span class="hljs-title function_">lazy</span>(<span class="hljs-function">() =></span> <span class="hljs-keyword">import</span>(<span class="hljs-string">'./routes/Home'</span>));
<span class="hljs-keyword">const</span> <span class="hljs-title class_">About</span> = <span class="hljs-title function_">lazy</span>(<span class="hljs-function">() =></span> <span class="hljs-keyword">import</span>(<span class="hljs-string">'./routes/About'</span>));
<span class="hljs-keyword">const</span> <span class="hljs-title function_">App</span> = (<span class="hljs-params"></span>) => (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Router</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">Suspense</span> <span class="hljs-attr">fallback</span>=<span class="hljs-string">{</span>&#x3C;<span class="hljs-attr">div</span>></span>Loading...<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>}>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Switch</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> <span class="hljs-attr">exact</span> <span class="hljs-attr">path</span>=<span class="hljs-string">'/'</span> <span class="hljs-attr">component</span>=<span class="hljs-string">{Home}</span> /></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span> <span class="hljs-attr">path</span>=<span class="hljs-string">'/about'</span> <span class="hljs-attr">component</span>=<span class="hljs-string">{About}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">Switch</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">Suspense</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">Router</span>></span></span>
);
</code></pre>
<!-- codeblock-end -->

In the above code, the code splitting will happen at each route level.

========== Id ==========  
200

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#200-What-is-route-based-code-splitting

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
