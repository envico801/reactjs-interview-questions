========== Question ==========  

### What is the use of the `ownProps` parameter in `mapStateToProps()` and `mapDispatchToProps()`?  

========== Answer ==========  

If the `ownProps` parameter is specified, React Redux will pass the props that were passed to the component into your _connect_ functions. So, if you use a connected component:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">ConnectedComponent</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./containers/ConnectedComponent'</span>;
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ConnectedComponent</span> <span class="hljs-attr">user</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">john</span>'} /></span></span>;
</code></pre>
<!-- codeblock-end -->

The `ownProps` inside your `mapStateToProps()` and `mapDispatchToProps()` functions will be an object:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">{
    <span class="hljs-attr">user</span>: <span class="hljs-string">'john'</span>;
}
</code></pre>
<!-- codeblock-end -->

You can use this object to decide what to return from those functions.

========== Id ==========  
120

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#120-What-is-the-use-of-the-ownprops-paramete

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
