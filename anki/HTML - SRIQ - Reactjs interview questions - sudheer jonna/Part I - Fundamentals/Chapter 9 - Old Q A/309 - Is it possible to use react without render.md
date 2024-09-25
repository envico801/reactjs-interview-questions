========== Question ==========  

### Is it possible to use React without rendering HTML?  

========== Answer ==========  

It is possible. Below are the possible options:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-literal">false</span>
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-literal">true</span>
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-literal">null</span>
}
</code></pre>
<!-- codeblock-end -->

React version >=16.0.0:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> []
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-string">""</span>
}
</code></pre>
<!-- codeblock-end -->

React version >=16.2.0:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">React.Fragment</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">React.Fragment</span>></span></span>
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;></span><span class="hljs-tag">&#x3C;/></span></span>
}
</code></pre>
<!-- codeblock-end -->

React version >=18.0.0:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-literal">undefined</span>
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
309

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#309-Is-it-possible-to-use-react-without-render

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
