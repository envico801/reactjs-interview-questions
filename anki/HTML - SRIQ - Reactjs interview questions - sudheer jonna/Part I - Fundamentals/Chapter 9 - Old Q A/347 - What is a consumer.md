========== Question ==========  

### What is a consumer?  

========== Answer ==========  

A Consumer is a React component that subscribes to context changes. It requires a function as a child which receives current context value as argument and returns a react node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree.

Lets take a simple example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">MyContext</span>.<span class="hljs-property">Consumer</span>>
  {<span class="hljs-function"><span class="hljs-params">value</span> =></span> <span class="hljs-comment">/* render something based on the context value */</span>}
&#x3C;/<span class="hljs-title class_">MyContext</span>.<span class="hljs-property">Consumer</span>>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
347

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#347-What-is-a-consumer

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
