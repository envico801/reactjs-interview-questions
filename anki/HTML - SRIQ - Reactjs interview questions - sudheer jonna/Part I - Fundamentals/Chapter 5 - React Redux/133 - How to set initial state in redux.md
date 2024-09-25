========== Question ==========  

### How to set initial state in Redux?  

========== Answer ==========  

You need to pass initial state as second argument to createStore:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> rootReducer = <span class="hljs-title function_">combineReducers</span>({
    <span class="hljs-attr">todos</span>: todos,
    <span class="hljs-attr">visibilityFilter</span>: visibilityFilter,
});
<span class="hljs-keyword">const</span> initialState = {
    <span class="hljs-attr">todos</span>: [{ <span class="hljs-attr">id</span>: <span class="hljs-number">123</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'example'</span>, <span class="hljs-attr">completed</span>: <span class="hljs-literal">false</span> }],
};
<span class="hljs-keyword">const</span> store = <span class="hljs-title function_">createStore</span>(rootReducer, initialState);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
133

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#133-How-to-set-initial-state-in-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
