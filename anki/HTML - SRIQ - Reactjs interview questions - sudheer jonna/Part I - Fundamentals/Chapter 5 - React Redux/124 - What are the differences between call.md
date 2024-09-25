========== Question ==========  

### What are the differences between `call()` and `put()` in redux-saga?  

========== Answer ==========  

Both `call()` and `put()` are effect creator functions. `call()` function is used to create effect description, which instructs middleware to call the promise. `put()` function creates an effect, which instructs middleware to dispatch an action to the store.

Let's take example of how these effects work for fetching particular user data.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span>* <span class="hljs-title function_">fetchUserSaga</span>(<span class="hljs-params">action</span>) {
    <span class="hljs-comment">// `call` function accepts rest arguments, which will be passed to `api.fetchUser` function.</span>
    <span class="hljs-comment">// Instructing middleware to call promise, it resolved value will be assigned to `userData` variable</span>
    <span class="hljs-keyword">const</span> userData = <span class="hljs-keyword">yield</span> <span class="hljs-title function_">call</span>(api.<span class="hljs-property">fetchUser</span>, action.<span class="hljs-property">userId</span>);
    <span class="hljs-comment">// Instructing middleware to dispatch corresponding action.</span>
    <span class="hljs-keyword">yield</span> <span class="hljs-title function_">put</span>({
        <span class="hljs-attr">type</span>: <span class="hljs-string">'FETCH_USER_SUCCESS'</span>,
        userData,
    });
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
124

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#124-What-are-the-differences-between-call

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
