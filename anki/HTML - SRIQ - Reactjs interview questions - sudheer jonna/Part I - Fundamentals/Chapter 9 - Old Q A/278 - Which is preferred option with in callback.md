========== Question ==========  

### Which is preferred option with in callback refs and findDOMNode()?  

========== Answer ==========  

It is preferred to use _callback refs_ over `findDOMNode()` API. Because `findDOMNode()` prevents certain improvements in React in the future.

The **legacy** approach of using `findDOMNode`:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-title function_">findDOMNode</span>(<span class="hljs-variable language_">this</span>).<span class="hljs-title function_">scrollIntoView</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

The recommended approach is:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">node</span> = <span class="hljs-title function_">createRef</span>();
    }
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">node</span>.<span class="hljs-property">current</span>.<span class="hljs-title function_">scrollIntoView</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.node}</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
278

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#278-Which-is-preferred-option-with-in-callback

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
