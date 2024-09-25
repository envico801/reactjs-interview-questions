========== Question ==========  

### How do you solve performance corner cases while using context?  

========== Answer ==========  

The context uses reference identity to determine when to re-render, there are some gotchas that could trigger unintentional renders in consumers when a provider’s parent re-renders.

For example, the code below will re-render all consumers every time the Provider re-renders because a new object is always created for value.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Provider</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{{</span> <span class="hljs-attr">something:</span> '<span class="hljs-attr">something</span>' }}></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Toolbar</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">Provider</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

This can be solved by lifting up the value to parent state,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">value</span>: { <span class="hljs-attr">something</span>: <span class="hljs-string">'something'</span> },
        };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Provider</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{this.state.value}</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Toolbar</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">Provider</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
348

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#348-How-do-you-solve-performance-corner-cases

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
