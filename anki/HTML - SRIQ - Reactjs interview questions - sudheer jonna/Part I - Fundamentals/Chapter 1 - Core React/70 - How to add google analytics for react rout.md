========== Question ==========  

### How to add Google Analytics for React Router?  

========== Answer ==========  

Add a listener on the `history` object to record each page view:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">history.<span class="hljs-title function_">listen</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">location</span>) {
    <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">ga</span>(<span class="hljs-string">'set'</span>, <span class="hljs-string">'page'</span>, location.<span class="hljs-property">pathname</span> + location.<span class="hljs-property">search</span>);
    <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">ga</span>(<span class="hljs-string">'send'</span>, <span class="hljs-string">'pageview'</span>, location.<span class="hljs-property">pathname</span> + location.<span class="hljs-property">search</span>);
});
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
70

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#70-How-to-add-google-analytics-for-react-rout

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
