========== Question ==========  

### What are error boundaries in React v16?  

========== Answer ==========  

_Error boundaries_ are components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.

A class component becomes an error boundary if it defines a new lifecycle method called `componentDidCatch(error, info)` or `static getDerivedStateFromError() `:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">ErrorBoundary</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">hasError</span>: <span class="hljs-literal">false</span> };
    }
    <span class="hljs-title function_">componentDidCatch</span>(<span class="hljs-params">error, info</span>) {
        <span class="hljs-comment">// You can also log the error to an error reporting service</span>
        <span class="hljs-title function_">logErrorToMyService</span>(error, info);
    }
    <span class="hljs-keyword">static</span> <span class="hljs-title function_">getDerivedStateFromError</span>(<span class="hljs-params">error</span>) {
        <span class="hljs-comment">// Update state so the next render will show the fallback UI.</span>
        <span class="hljs-keyword">return</span> { <span class="hljs-attr">hasError</span>: <span class="hljs-literal">true</span> };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">hasError</span>) {
            <span class="hljs-comment">// You can render any custom fallback UI</span>
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{'Something went wrong.'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
        }
        <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">children</span>;
    }
}
</code></pre>
<!-- codeblock-end -->

After that use it as a regular component:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">ErrorBoundary</span>>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyWidget</span> /></span></span>
&#x3C;/<span class="hljs-title class_">ErrorBoundary</span>>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
287

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#287-What-are-error-boundaries-in-react-v16

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
