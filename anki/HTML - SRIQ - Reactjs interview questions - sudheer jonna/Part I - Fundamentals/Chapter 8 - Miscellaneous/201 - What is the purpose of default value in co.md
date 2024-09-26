========== Question ==========  

### What is the purpose of default value in context?  

========== Answer ==========  

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them.

Below code snippet provides default theme value as Luna.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MyContext</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createContext</span>(defaultValue);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
201

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#201-What-is-the-purpose-of-default-value-in-co

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store