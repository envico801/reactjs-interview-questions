========== Question ==========  

### What is the impact of indexes as keys?  

========== Answer ==========  

Keys should be stable, predictable, and unique so that React can keep track of elements.

In the below code snippet each element's key will be based on ordering, rather than tied to the data that is being represented. This limits the optimizations that React can do and creates confusing bugs in the application.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">{
    todos.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">todo, index</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Todo</span> {<span class="hljs-attr">...todo</span>} <span class="hljs-attr">key</span>=<span class="hljs-string">{index}</span> /></span></span>);
}
</code></pre>
<!-- codeblock-end -->

If you use element data for unique key, assuming `todo.id` is unique to this list and stable, React would be able to reorder elements without needing to reevaluate them as much.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">{
    todos.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">todo</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Todo</span> {<span class="hljs-attr">...todo</span>} <span class="hljs-attr">key</span>=<span class="hljs-string">{todo.id}</span> /></span></span>);
}
</code></pre>
<!-- codeblock-end -->

**Note:** If you don't specify `key` prop at all, React will use index as a key's value while iterating over an array of data.

========== Id ==========  
45

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#45-What-is-the-impact-of-indexes-as-keys

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
