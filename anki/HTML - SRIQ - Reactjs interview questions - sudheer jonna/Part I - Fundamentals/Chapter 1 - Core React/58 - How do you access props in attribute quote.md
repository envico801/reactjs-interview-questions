========== Question ==========  

### How do you access props in attribute quotes?  

========== Answer ==========  

React (or JSX) doesn't support variable interpolation inside an attribute value. The below representation won't work:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;img className=<span class="hljs-string">'image'</span> src=<span class="hljs-string">'images/{this.props.image}'</span> />
</code></pre>
<!-- codeblock-end -->

But you can put any JS expression inside curly braces as the entire attribute value. So the below expression works:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;img className=<span class="hljs-string">'image'</span> src={<span class="hljs-string">'images/'</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">image</span>} />
</code></pre>
<!-- codeblock-end -->

Using _template strings_ will also work:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;img className=<span class="hljs-string">'image'</span> src={<span class="hljs-string">`images/<span class="hljs-subst">${<span class="hljs-variable language_">this</span>.props.image}</span>`</span>} />
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
58

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#58-How-do-you-access-props-in-attribute-quote

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
