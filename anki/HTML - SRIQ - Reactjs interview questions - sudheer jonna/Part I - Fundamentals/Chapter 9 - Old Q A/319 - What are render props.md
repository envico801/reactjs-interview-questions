========== Question ==========  

### What are render props?  

========== Answer ==========  

**Render Props** is a simple technique for sharing code between components using a prop whose value is a function. The below component uses render prop which returns a React element.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">DataProvider</span> render={<span class="hljs-function">(<span class="hljs-params">data</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{`Hello ${data.target}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>} />
</code></pre>
<!-- codeblock-end -->

Libraries such as React Router and DownShift are using this pattern.

========== Id ==========  
319

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#319-What-are-render-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
