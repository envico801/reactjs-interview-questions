========== Question ==========  

### What is "key" prop and what is the benefit of using it in arrays of elements?  

========== Answer ==========  

A `key` is a special attribute you **should** include when mapping over arrays to render data. _Key_ prop helps React identify which items have changed, are added, or are removed.

Keys should be unique among its siblings. Most often we use ID from our data as _key_:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> todoItems = todos.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">todo</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{todo.id}</span>></span>{todo.text}<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>);
</code></pre>
<!-- codeblock-end -->

When you don't have stable IDs for rendered items, you may use the item _index_ as a _key_ as a last resort:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> todoItems = todos.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">todo, index</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{index}</span>></span>{todo.text}<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>);
</code></pre>
<!-- codeblock-end -->

**Note:**

1. Using _indexes_ for _keys_ is **not recommended** if the order of items may change. This can negatively impact performance and may cause issues with component state.

2. If you extract list item as separate component then apply _keys_ on list component instead of `li` tag.

3. There will be a warning message in the console if the `key` prop is not present on list items.

4. The key attribute accepts either string or number and internally convert it as string type.

5. Don't generate the key on the fly something like `key={Math.random()}`. Because the keys will never match up between re-renders and DOM created everytime.

========== Id ==========  
15

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#15-What-is-key-prop-and-what-is-the-benefit

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
