========== Question ==========  

### How to conditionally apply class attributes?  

========== Answer ==========  

You shouldn't use curly braces inside quotes because it is going to be evaluated as a string.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;div className=<span class="hljs-string">"btn-panel {this.props.visible ? 'show' : 'hidden'}"</span>>
</code></pre>
<!-- codeblock-end -->

Instead you need to move curly braces outside (don't forget to include spaces between class names):

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;div className={<span class="hljs-string">'btn-panel '</span> + (<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">visible</span> ? <span class="hljs-string">'show'</span> : <span class="hljs-string">'hidden'</span>)}>
</code></pre>
<!-- codeblock-end -->

_Template strings_ will also work:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;div className={<span class="hljs-string">`btn-panel <span class="hljs-subst">${<span class="hljs-variable language_">this</span>.props.visible ? <span class="hljs-string">'show'</span> : <span class="hljs-string">'hidden'</span>}</span>`</span>}>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
60

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#60-How-to-conditionally-apply-class-attribute

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
