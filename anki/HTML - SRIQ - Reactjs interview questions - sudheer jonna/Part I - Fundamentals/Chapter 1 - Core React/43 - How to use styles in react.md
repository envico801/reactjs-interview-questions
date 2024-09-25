========== Question ==========  

### How to use styles in React?  

========== Answer ==========  

The `style` attribute accepts a JavaScript object with camelCased properties rather than a CSS string. This is consistent with the DOM style JavaScript property, is more efficient, and prevents XSS security holes.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> divStyle = {
    <span class="hljs-attr">color</span>: <span class="hljs-string">'blue'</span>,
    <span class="hljs-attr">backgroundImage</span>: <span class="hljs-string">'url('</span> + imgUrl + <span class="hljs-string">')'</span>,
};
<span class="hljs-keyword">function</span> <span class="hljs-title function_">HelloWorldComponent</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">style</span>=<span class="hljs-string">{divStyle}</span>></span>Hello World!<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

Style keys are camelCased in order to be consistent with accessing the properties on DOM nodes in JavaScript (e.g. `node.style.backgroundImage`).

========== Id ==========  
43

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#43-How-to-use-styles-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
