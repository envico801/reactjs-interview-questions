========== Question ==========  

### How to create props proxy for HOC component?  

========== Answer ==========  

You can add/edit props passed to the component using _props proxy_ pattern like this:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">HOC</span>(<span class="hljs-params">WrappedComponent</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">Test</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">const</span> newProps = {
                <span class="hljs-attr">title</span>: <span class="hljs-string">'New Header'</span>,
                <span class="hljs-attr">footer</span>: <span class="hljs-literal">false</span>,
                <span class="hljs-attr">showFeatureX</span>: <span class="hljs-literal">false</span>,
                <span class="hljs-attr">showFeatureY</span>: <span class="hljs-literal">true</span>,
            };
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">WrappedComponent</span> {<span class="hljs-attr">...this.props</span>} {<span class="hljs-attr">...newProps</span>} /></span></span>;
        }
    };
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
282

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#282-How-to-create-props-proxy-for-hoc-componen

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
