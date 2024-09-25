========== Question ==========  

### What are the exceptions on React component naming?  

========== Answer ==========  

The component names should start with an uppercase letter but there are few exceptions to this convention. The lowercase tag names with a dot (property accessors) are still considered as valid component names.

For example, the below tag can be compiled to a valid component,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">     <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
          <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">obj.component</span>/></span></span> <span class="hljs-comment">// `React.createElement(obj.component)`</span>
          )
    }
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
73

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#73-What-are-the-exceptions-on-react-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
