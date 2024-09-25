========== Question ==========  

### What is dynamic import?  

========== Answer ==========  

You can achieve code-splitting in your app using dynamic import.

Let's take an example of addition,

1.  **Normal Import**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { add } <span class="hljs-keyword">from</span> <span class="hljs-string">'./math'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">add</span>(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>));
</code></pre>
<!-- codeblock-end -->

2.  **Dynamic Import**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span>(<span class="hljs-string">'./math'</span>).<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">math</span>) =></span> {
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(math.<span class="hljs-title function_">add</span>(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>));
});
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
197

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#197-What-is-dynamic-import

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
