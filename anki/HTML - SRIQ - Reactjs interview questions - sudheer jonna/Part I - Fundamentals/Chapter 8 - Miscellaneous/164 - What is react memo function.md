========== Question ==========  

### What is React memo function?  

========== Answer ==========  

Class components can be restricted from re-rendering when their input props are the same using **PureComponent or shouldComponentUpdate**. Now you can do the same with function components by wrapping them in **React.memo**.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MyComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">memo</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">MyComponent</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-comment">/* only rerenders if props change */</span>
});
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
164

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#164-What-is-react-memo-function

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
