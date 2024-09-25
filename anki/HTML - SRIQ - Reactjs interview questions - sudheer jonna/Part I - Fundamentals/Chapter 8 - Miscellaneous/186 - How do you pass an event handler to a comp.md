========== Question ==========  

### How do you pass an event handler to a component?  

========== Answer ==========  

You can pass event handlers and other functions as props to child components. The functions can be passed to child component as below,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Button</span>(<span class="hljs-params">{ onClick }</span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{onClick}</span>></span>Download<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>;
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">downloadExcel</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
        <span class="hljs-title function_">alert</span>(<span class="hljs-string">'Downloaded'</span>);
    }
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleClick}</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">Button</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
186

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#186-How-do-you-pass-an-event-handler-to-a-comp

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
