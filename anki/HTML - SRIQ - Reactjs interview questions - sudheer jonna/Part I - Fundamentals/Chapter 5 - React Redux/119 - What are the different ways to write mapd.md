========== Question ==========  

### What are the different ways to write `mapDispatchToProps()`?  

========== Answer ==========  

There are a few ways of binding _action creators_ to `dispatch()` in `mapDispatchToProps()`.

Below are the possible options:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">mapDispatchToProps</span> = (<span class="hljs-params">dispatch</span>) => ({
    <span class="hljs-attr">action</span>: <span class="hljs-function">() =></span> <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">action</span>()),
});
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">mapDispatchToProps</span> = (<span class="hljs-params">dispatch</span>) => ({
    <span class="hljs-attr">action</span>: <span class="hljs-title function_">bindActionCreators</span>(action, dispatch),
});
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> mapDispatchToProps = { action };
</code></pre>
<!-- codeblock-end -->

The third option is just a shorthand for the first one.

========== Id ==========  
119

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#119-What-are-the-different-ways-to-write-mapd

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
