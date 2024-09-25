========== Question ==========  

### What are HOC factory implementations?  

========== Answer ==========  

There are two main ways of implementing HOCs in React.

1.  Props Proxy (PP) and

2.  Inheritance Inversion (II).

But they follow different approaches for manipulating the _WrappedComponent_.

**Props Proxy**

In this approach, the render method of the HOC returns a React Element of the type of the WrappedComponent. We also pass through the props that the HOC receives, hence the name **Props Proxy**.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">ppHOC</span>(<span class="hljs-params">WrappedComponent</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">PP</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">WrappedComponent</span> {<span class="hljs-attr">...this.props</span>} /></span></span>;
        }
    };
}
</code></pre>
<!-- codeblock-end -->

**Inheritance Inversion**

In this approach, the returned HOC class (Enhancer) extends the WrappedComponent. It is called Inheritance Inversion because instead of the WrappedComponent extending some Enhancer class, it is passively extended by the Enhancer. In this way the relationship between them seems **inverse**.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">iiHOC</span>(<span class="hljs-params">WrappedComponent</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">Enhancer</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">WrappedComponent</span> {
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">return</span> <span class="hljs-variable language_">super</span>.<span class="hljs-title function_">render</span>();
        }
    };
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
326

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#326-What-are-hoc-factory-implementations

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
