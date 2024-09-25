========== Question ==========  

### What is the recommended way for naming components?  

========== Answer ==========  

It is recommended to name the component by reference instead of using `displayName`.

Using `displayName` for naming component:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createClass</span>({
    <span class="hljs-attr">displayName</span>: <span class="hljs-string">'TodoApp'</span>,
    <span class="hljs-comment">// ...</span>
});
</code></pre>
<!-- codeblock-end -->

The **recommended** approach:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">TodoApp</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-comment">// ...</span>
}
</code></pre>
<!-- codeblock-end -->

also

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">TodoApp</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-comment">//...</span>
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">TodoApp</span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
299

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#299-What-is-the-recommended-way-for-naming-com

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
