========== Question ==========  

### How to import and export components using React and ES6?  

========== Answer ==========  

You should use default for exporting the components

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">from</span> <span class="hljs-string">"user"</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title class_">MyProfile</span> {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">User</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"customer"</span>></span>//...<span class="hljs-tag">&#x3C;/<span class="hljs-name">User</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

<details><summary><b>See Class</b></summary>

<p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'user'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyProfile</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">User</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'customer'</span>></span>//...<span class="hljs-tag">&#x3C;/<span class="hljs-name">User</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

</p>

</details>

With the export specifier, the MyProfile is going to be the member and exported to this module and the same can be imported without mentioning the name in other components.

========== Id ==========  
72

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#72-How-to-import-and-export-components-using

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
