========== Question ==========  

### What are Redux selectors and why use them?  

========== Answer ==========  

_Selectors_ are functions that take Redux state as an argument and return some data to pass to the component.

For example, to get user details from the state:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">getUserData</span> = (<span class="hljs-params">state</span>) => state.<span class="hljs-property">user</span>.<span class="hljs-property">data</span>;
</code></pre>
<!-- codeblock-end -->

These selectors have two main benefits,

1.  The selector can compute derived data, allowing Redux to store the minimal possible state

2.  The selector is not recomputed unless one of its arguments changes

========== Id ==========  
129

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#129-What-are-redux-selectors-and-why-use-them

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
