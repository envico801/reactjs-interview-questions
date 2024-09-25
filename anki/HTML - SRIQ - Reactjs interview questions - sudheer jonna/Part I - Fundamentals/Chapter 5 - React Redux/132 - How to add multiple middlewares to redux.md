========== Question ==========  

### How to add multiple middlewares to Redux?  

========== Answer ==========  

You can use `applyMiddleware()`.

For example, you can add `redux-thunk` and `logger` passing them as arguments to `applyMiddleware()`:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { createStore, applyMiddleware } <span class="hljs-keyword">from</span> <span class="hljs-string">'redux'</span>;
<span class="hljs-keyword">const</span> createStoreWithMiddleware = <span class="hljs-title function_">applyMiddleware</span>(<span class="hljs-title class_">ReduxThunk</span>, logger)(createStore);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
132

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#132-How-to-add-multiple-middlewares-to-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
