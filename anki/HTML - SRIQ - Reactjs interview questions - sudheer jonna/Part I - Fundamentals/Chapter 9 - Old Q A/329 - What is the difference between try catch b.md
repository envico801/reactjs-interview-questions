========== Question ==========  

### What is the difference between try catch block and error boundaries?  

========== Answer ==========  

Try catch block works with imperative code whereas error boundaries are meant for declarative code to render on the screen.

For example, the try catch block used for below imperative code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">try</span> {
    <span class="hljs-title function_">showButton</span>();
} <span class="hljs-keyword">catch</span> (error) {
    <span class="hljs-comment">// ...</span>
}
</code></pre>
<!-- codeblock-end -->

Whereas error boundaries wrap declarative code as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">ErrorBoundary</span>>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyComponent</span> /></span></span>
&#x3C;/<span class="hljs-title class_">ErrorBoundary</span>>
</code></pre>
<!-- codeblock-end -->

So if an error occurs in a **componentDidUpdate** method caused by a **setState** somewhere deep in the tree, it will still correctly propagate to the closest error boundary.

========== Id ==========  
329

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#329-What-is-the-difference-between-try-catch-b

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
