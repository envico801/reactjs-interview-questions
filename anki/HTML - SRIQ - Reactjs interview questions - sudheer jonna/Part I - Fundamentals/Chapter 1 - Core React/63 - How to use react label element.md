========== Question ==========  

### How to use React label element?  

========== Answer ==========  

If you try to render a `<label>` element bound to a text input using the standard `for` attribute, then it produces HTML missing that attribute and prints a warning to the console.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;label <span class="hljs-keyword">for</span>={<span class="hljs-string">'user'</span>}>{<span class="hljs-string">'User'</span>}&#x3C;/label>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">text</span>'} <span class="hljs-attr">id</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">user</span>'} /></span></span>
</code></pre>
<!-- codeblock-end -->

Since `for` is a reserved keyword in JavaScript, use `htmlFor` instead.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;label htmlFor={<span class="hljs-string">'user'</span>}>{<span class="hljs-string">'User'</span>}&#x3C;/label>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">text</span>'} <span class="hljs-attr">id</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">user</span>'} /></span></span>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
63

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#63-How-to-use-react-label-element

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
