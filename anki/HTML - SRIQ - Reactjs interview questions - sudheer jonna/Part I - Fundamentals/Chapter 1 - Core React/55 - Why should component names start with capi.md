========== Question ==========  

### Why should component names start with capital letter?  

========== Answer ==========  

If you are rendering your component using JSX, the name of that component has to begin with a capital letter otherwise React will throw an error as an unrecognized tag. This convention is because only HTML elements and SVG tags can begin with a lowercase letter.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title class_">SomeComponent</span> {
  <span class="hljs-comment">// Code goes here</span>
}
</code></pre>
<!-- codeblock-end -->

You can define function component whose name starts with lowercase letter, but when it's imported it should have a capital letter. Here lowercase is fine:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> myComponent {
  <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> /></span></span>;
  }
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> myComponent;
</code></pre>
<!-- codeblock-end -->

While when imported in another file it should start with capital letter:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./myComponent'</span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
55

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#55-Why-should-component-names-start-with-capi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
