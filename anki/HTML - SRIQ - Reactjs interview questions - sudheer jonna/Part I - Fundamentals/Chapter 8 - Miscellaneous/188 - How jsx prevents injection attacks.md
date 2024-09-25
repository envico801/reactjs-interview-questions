========== Question ==========  

### How JSX prevents Injection Attacks?  

========== Answer ==========  

React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered.

For example, you can embed user input as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> name = response.<span class="hljs-property">potentiallyMaliciousInput</span>;
<span class="hljs-keyword">const</span> element = <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
</code></pre>
<!-- codeblock-end -->

This way you can prevent XSS(Cross-site-scripting) attacks in the application.

========== Id ==========  
188

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#188-How-jsx-prevents-injection-attacks

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
