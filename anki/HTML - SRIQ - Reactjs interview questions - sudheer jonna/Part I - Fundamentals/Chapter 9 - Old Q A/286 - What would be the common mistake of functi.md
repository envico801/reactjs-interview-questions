========== Question ==========  

### What would be the common mistake of function being called every time the component renders?  

========== Answer ==========  

You need to make sure that function is not being called while passing the function as a parameter.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Wrong: handleClick is called instead of passed as a reference!</span>
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick()}</span>></span>{'Click Me'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
}
</code></pre>
<!-- codeblock-end -->

Instead, pass the function itself without parenthesis:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-comment">// Correct: handleClick is passed as a reference!</span>
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick}</span>></span>{'Click Me'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
286

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#286-What-would-be-the-common-mistake-of-functi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
