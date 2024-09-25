========== Question ==========  

### How to pass params to `history.push` method in React Router v4?  

========== Answer ==========  

While navigating you can pass props to the `history` object:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">history</span>.<span class="hljs-title function_">push</span>({
    <span class="hljs-attr">pathname</span>: <span class="hljs-string">'/template'</span>,
    <span class="hljs-attr">search</span>: <span class="hljs-string">'?name=sudheer'</span>,
    <span class="hljs-attr">state</span>: { <span class="hljs-attr">detail</span>: response.<span class="hljs-property">data</span> },
});
</code></pre>
<!-- codeblock-end -->

The `search` property is used to pass query params in `push()` method.

========== Id ==========  
86

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#86-How-to-pass-params-to-history-push-metho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
