========== Question ==========  

### How can we find the version of React at runtime in the browser?  

========== Answer ==========  

You can use `React.version` to get the version.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-variable constant_">REACT_VERSION</span> = <span class="hljs-title class_">React</span>.<span class="hljs-property">version</span>;
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{`React version: ${REACT_VERSION}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'app'</span>));
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
69

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#69-How-can-we-find-the-version-of-react-at-ru

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
