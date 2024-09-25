========== Question ==========  

### How to set state with a dynamic key name?  

========== Answer ==========  

If you are using ES6 or the Babel transpiler to transform your JSX code then you can accomplish this with _computed property names_.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">handleInputChange</span>(<span class="hljs-params">event</span>) {
  <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ [event.<span class="hljs-property">target</span>.<span class="hljs-property">id</span>]: event.<span class="hljs-property">target</span>.<span class="hljs-property">value</span> })
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
285

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#285-How-to-set-state-with-a-dynamic-key-name

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
