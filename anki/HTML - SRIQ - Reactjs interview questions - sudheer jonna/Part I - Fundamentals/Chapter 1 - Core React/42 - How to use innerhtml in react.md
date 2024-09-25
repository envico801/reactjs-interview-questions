========== Question ==========  

### How to use innerHTML in React?  

========== Answer ==========  

The `dangerouslySetInnerHTML` attribute is React's replacement for using `innerHTML` in the browser DOM. Just like `innerHTML`, it is risky to use this attribute considering cross-site scripting (XSS) attacks. You just need to pass a `__html` object as key and HTML text as value.

In this example MyComponent uses `dangerouslySetInnerHTML` attribute for setting HTML markup:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">createMarkup</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> { <span class="hljs-attr">__html</span>: <span class="hljs-string">'First &#x26;middot; Second'</span> };
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">MyComponent</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">dangerouslySetInnerHTML</span>=<span class="hljs-string">{createMarkup()}</span> /></span></span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
42

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#42-How-to-use-innerhtml-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
