========== Question ==========  

### What is the purpose of getDerivedStateFromError?  

========== Answer ==========  

This lifecycle method is invoked after an error has been thrown by a descendant component. It receives the error that was thrown as a parameter and should return a value to update state.

The signature of the lifecycle method is as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">static</span> <span class="hljs-title function_">getDerivedStateFromError</span>(error)
</code></pre>
<!-- codeblock-end -->

Let us take error boundary use case with the above lifecycle method for demonstration purpose,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">ErrorBoundary</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">hasError</span>: <span class="hljs-literal">false</span> };
    }
    <span class="hljs-keyword">static</span> <span class="hljs-title function_">getDerivedStateFromError</span>(<span class="hljs-params">error</span>) {
        <span class="hljs-comment">// Update state so the next render will show the fallback UI.</span>
        <span class="hljs-keyword">return</span> { <span class="hljs-attr">hasError</span>: <span class="hljs-literal">true</span> };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">hasError</span>) {
            <span class="hljs-comment">// You can render any custom fallback UI</span>
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Something went wrong.<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
        }
        <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">children</span>;
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
335

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#335-What-is-the-purpose-of-getderivedstatefrom

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
