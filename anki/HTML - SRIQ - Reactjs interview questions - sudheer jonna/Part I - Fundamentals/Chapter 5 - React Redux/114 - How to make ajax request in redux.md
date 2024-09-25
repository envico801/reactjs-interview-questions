========== Question ==========  

### How to make AJAX request in Redux?  

========== Answer ==========  

You can use `redux-thunk` middleware which allows you to define async actions.

Let's take an example of fetching specific account as an AJAX call using _fetch API_:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">fetchAccount</span>(<span class="hljs-params">id</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-function">(<span class="hljs-params">dispatch</span>) =></span> {
        <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">setLoadingAccountState</span>()); <span class="hljs-comment">// Show a loading spinner</span>
        <span class="hljs-title function_">fetch</span>(<span class="hljs-string">`/account/<span class="hljs-subst">${id}</span>`</span>, <span class="hljs-function">(<span class="hljs-params">response</span>) =></span> {
            <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">doneFetchingAccount</span>()); <span class="hljs-comment">// Hide loading spinner</span>
            <span class="hljs-keyword">if</span> (response.<span class="hljs-property">status</span> === <span class="hljs-number">200</span>) {
                <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">setAccount</span>(response.<span class="hljs-property">json</span>)); <span class="hljs-comment">// Use a normal function to set the received state</span>
            } <span class="hljs-keyword">else</span> {
                <span class="hljs-title function_">dispatch</span>(someError);
            }
        });
    };
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">setAccount</span>(<span class="hljs-params">data</span>) {
    <span class="hljs-keyword">return</span> { <span class="hljs-attr">type</span>: <span class="hljs-string">'SET_Account'</span>, <span class="hljs-attr">data</span>: data };
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
114

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#114-How-to-make-ajax-request-in-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
