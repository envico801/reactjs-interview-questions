========== Question ==========  

### What are synthetic events in React?  

========== Answer ==========  

`SyntheticEvent` is a cross-browser wrapper around the browser's native event. Its API is same as the browser's native event, including `stopPropagation()` and `preventDefault()`, except the events work identically across all browsers. The native events can be accessed directly from synthetic events using `nativeEvent` attribute.

Let's take an example of BookStore title search component with the ability to get all native event properties

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">BookStore</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleTitleChange</span>(<span class="hljs-params">e</span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'The new title is:'</span>, e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>);
        <span class="hljs-comment">// 'e' represents synthetic event</span>
        <span class="hljs-keyword">const</span> nativeEvent = e.<span class="hljs-property">nativeEvent</span>;
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(nativeEvent);
        e.<span class="hljs-title function_">stopPropagation</span>();
        e.<span class="hljs-title function_">preventDefault</span>();
    }
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'title'</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{handleTitleChange}</span> /></span></span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
13

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#13-What-are-synthetic-events-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
