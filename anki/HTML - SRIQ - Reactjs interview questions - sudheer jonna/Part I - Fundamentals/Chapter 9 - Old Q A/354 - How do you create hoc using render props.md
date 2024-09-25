========== Question ==========  

### How do you create HOC using render props?  

========== Answer ==========  

You can implement most higher-order components (HOC) using a regular component with a render prop. For example, if you would prefer to have a withMouse HOC instead of a <Mouse> component, you could easily create one using a regular <Mouse> with a render prop.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">withMouse</span>(<span class="hljs-params">Component</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">extends</span> <span class="hljs-title class_">React</span>.<span class="hljs-property">Component</span> {
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Mouse</span> <span class="hljs-attr">render</span>=<span class="hljs-string">{(mouse)</span> =></span> <span class="hljs-tag">&#x3C;<span class="hljs-name">Component</span> {<span class="hljs-attr">...this.props</span>} <span class="hljs-attr">mouse</span>=<span class="hljs-string">{mouse}</span> /></span>} /></span>;
        }
    };
}
</code></pre>
<!-- codeblock-end -->

This way render props gives the flexibility of using either pattern.

========== Id ==========  
354

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#354-How-do-you-create-hoc-using-render-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
