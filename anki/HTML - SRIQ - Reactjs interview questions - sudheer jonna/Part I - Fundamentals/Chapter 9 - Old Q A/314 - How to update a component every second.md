========== Question ==========  

### How to update a component every second?  

========== Answer ==========  

You need to use `setInterval()` to trigger the change, but you also need to clear the timer when the component unmounts to prevent errors and memory leaks.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
  <span class="hljs-variable language_">this</span>.<span class="hljs-property">interval</span> = <span class="hljs-built_in">setInterval</span>(<span class="hljs-function">() =></span> <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">time</span>: <span class="hljs-title class_">Date</span>.<span class="hljs-title function_">now</span>() }), <span class="hljs-number">1000</span>)
}
<span class="hljs-title function_">componentWillUnmount</span>(<span class="hljs-params"></span>) {
  <span class="hljs-built_in">clearInterval</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">interval</span>)
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
314

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#314-How-to-update-a-component-every-second

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
