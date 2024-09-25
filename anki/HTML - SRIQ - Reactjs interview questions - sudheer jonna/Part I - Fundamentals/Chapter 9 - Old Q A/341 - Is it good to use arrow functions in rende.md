========== Question ==========  

### Is it good to use arrow functions in render methods?  

========== Answer ==========  

Yes, You can use. It is often the easiest way to pass parameters to callback functions. But you need to optimize the performance while using it.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Foo</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Click happened'</span>);
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> this.handleClick()}>Click Me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

**Note:** Using an arrow function in render method creates a new function each time the component renders, which may have performance implications

========== Id ==========  
341

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#341-Is-it-good-to-use-arrow-functions-in-rende

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
