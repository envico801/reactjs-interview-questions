========== Question ==========  

### What is the main purpose of constructor?  

========== Answer ==========  

The constructor is mainly used for two purposes,

1.  To initialize local state by assigning object to this.state

2.  For binding event handler methods to the instance

    For example, the below code covers both the above cases,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
  <span class="hljs-variable language_">super</span>(props);
  <span class="hljs-comment">// Don't call this.setState() here!</span>
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">counter</span>: <span class="hljs-number">0</span> };
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span> = <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
332

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#332-What-is-the-main-purpose-of-constructor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
