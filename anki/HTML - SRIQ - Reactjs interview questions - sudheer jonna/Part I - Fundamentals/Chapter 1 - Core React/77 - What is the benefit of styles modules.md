========== Question ==========  

### What is the benefit of styles modules?  

========== Answer ==========  

It is recommended to avoid hard coding style values in components. Any values that are likely to be used across different UI components should be extracted into their own modules.

For example, these styles could be extracted into a separate component:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> colors = {
    white,
    black,
    blue,
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> space = [<span class="hljs-number">0</span>, <span class="hljs-number">8</span>, <span class="hljs-number">16</span>, <span class="hljs-number">32</span>, <span class="hljs-number">64</span>];
</code></pre>
<!-- codeblock-end -->

And then imported individually in other components:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { space, colors } <span class="hljs-keyword">from</span> <span class="hljs-string">'./styles'</span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
77

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#77-What-is-the-benefit-of-styles-modules

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
