========== Question ==========  

### What is Concurrent Rendering?  

========== Answer ==========  

The Concurrent rendering makes React apps to be more responsive by rendering component trees without blocking the main UI thread. It allows React to interrupt a long-running render to handle a high-priority event. i.e, When you enabled concurrent Mode, React will keep an eye on other tasks that need to be done, and if there's something with a higher priority it will pause what it is currently rendering and let the other task finish first. You can enable this in two ways,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// 1. Part of an app by wrapping with ConcurrentMode</span>
&#x3C;<span class="hljs-title class_">React</span>.<span class="hljs-property">unstable_ConcurrentMode</span>>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Something</span> /></span></span>
&#x3C;/<span class="hljs-title class_">React</span>.<span class="hljs-property">unstable_ConcurrentMode</span>>;
<span class="hljs-comment">// 2. Whole app using createRoot</span>
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">unstable_createRoot</span>(domNode).<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span></span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
230

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#230-What-is-concurrent-rendering

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
