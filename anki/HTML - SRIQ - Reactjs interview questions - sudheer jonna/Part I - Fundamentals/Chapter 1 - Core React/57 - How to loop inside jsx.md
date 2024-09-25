========== Question ==========  

### How to loop inside JSX?  

========== Answer ==========  

You can simply use `Array.prototype.map` with ES6 _arrow function_ syntax.

For example, the `items` array of objects is mapped into an array of components:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;tbody>
    {items.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">item</span>) =></span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">SomeComponent</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{item.id}</span> <span class="hljs-attr">name</span>=<span class="hljs-string">{item.name}</span> /></span></span>
    ))}
&#x3C;/tbody>
</code></pre>
<!-- codeblock-end -->

But you can't iterate using `for` loop:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;tbody>
  <span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> i = <span class="hljs-number">0</span>; i &#x3C; items.<span class="hljs-property">length</span>; i++) {
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">SomeComponent</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{items[i].id}</span> <span class="hljs-attr">name</span>=<span class="hljs-string">{items[i].name}</span> /></span></span>
  }
&#x3C;/tbody>
</code></pre>
<!-- codeblock-end -->

This is because JSX tags are transpiled into _function calls_, and you can't use statements inside expressions. This may change thanks to `do` expressions which are _stage 1 proposal_.

========== Id ==========  
57

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#57-How-to-loop-inside-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
