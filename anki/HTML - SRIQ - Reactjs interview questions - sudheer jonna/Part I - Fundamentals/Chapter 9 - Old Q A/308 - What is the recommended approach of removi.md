========== Question ==========  

### What is the recommended approach of removing an array element in React state?  

========== Answer ==========  

The better approach is to use `Array.prototype.filter()` method.

For example, let's create a `removeItem()` method for updating the state.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">removeItem</span>(<span class="hljs-params">index</span>) {
  <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
    <span class="hljs-attr">data</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">data</span>.<span class="hljs-title function_">filter</span>(<span class="hljs-function">(<span class="hljs-params">item, i</span>) =></span> i !== index)
  })
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
308

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#308-What-is-the-recommended-approach-of-removi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
