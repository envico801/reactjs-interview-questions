========== Question ==========  

### How to dispatch an action on load?  

========== Answer ==========  

You can dispatch an action in `componentDidMount()` method and in `render()` method you can verify the data.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-title function_">fetchData</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">isLoaded</span> ? <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{'Loaded'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span> : <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{'Not Loaded'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    }
}
<span class="hljs-keyword">const</span> <span class="hljs-title function_">mapStateToProps</span> = (<span class="hljs-params">state</span>) => ({
    <span class="hljs-attr">isLoaded</span>: state.<span class="hljs-property">isLoaded</span>,
});
<span class="hljs-keyword">const</span> mapDispatchToProps = { fetchData };
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">connect</span>(mapStateToProps, mapDispatchToProps)(<span class="hljs-title class_">App</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
320

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#320-How-to-dispatch-an-action-on-load

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
