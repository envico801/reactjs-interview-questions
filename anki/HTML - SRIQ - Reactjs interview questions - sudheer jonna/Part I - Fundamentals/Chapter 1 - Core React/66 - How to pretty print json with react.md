========== Question ==========  

### How to pretty print JSON with React?  

========== Answer ==========  

We can use `<pre>` tag so that the formatting of the `JSON.stringify()` is retained:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> data = { <span class="hljs-attr">name</span>: <span class="hljs-string">"John"</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">42</span> };
<span class="hljs-keyword">function</span> <span class="hljs-title class_">User</span> {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">pre</span>></span>{JSON.stringify(data, null, 2)}<span class="hljs-tag">&#x3C;/<span class="hljs-name">pre</span>></span></span>;
}
<span class="hljs-keyword">const</span> container = <span class="hljs-title function_">createRoot</span>(<span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">"container"</span>));
container.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">User</span> /></span></span>);
</code></pre>
<!-- codeblock-end -->

  <details><summary><b>See Class</b></summary>

  <p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> data = { <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">42</span> };
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">pre</span>></span>{JSON.stringify(data, null, 2)}<span class="hljs-tag">&#x3C;/<span class="hljs-name">pre</span>></span></span>;
    }
}
<span class="hljs-title class_">React</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">User</span> /></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'container'</span>));
</code></pre>
<!-- codeblock-end -->

  </p>

  </details>

========== Id ==========  
66

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#66-How-to-pretty-print-json-with-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
