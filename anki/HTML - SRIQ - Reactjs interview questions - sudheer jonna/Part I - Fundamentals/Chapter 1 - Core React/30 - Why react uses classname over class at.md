========== Question ==========  

### Why React uses `className` over `class` attribute?  

========== Answer ==========  

The attribute names written in JSX turned into keys of JavaScript objects and the JavaScript names cannot contain dashes or reversed words, it is recommended to use camelCase wherever applicable in JSX code. The attribute `class` is a keyword in JavaScript, and JSX is an extension of JavaScript. That's the principle reason why React uses `className` instead of `class`. Pass a string as the `className` prop.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">span</span> <span class="hljs-attr">className</span>=<span class="hljs-string">"menu navigation-menu"</span>></span>{'Menu'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span></span>
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
30

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#30-Why-react-uses-classname-over-class-at

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
