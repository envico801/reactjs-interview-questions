========== Question ==========  

### Is it possible to prevent automatic batching?  

========== Answer ==========  

Yes, it is possible to prevent automatic batching default behavior. There might be cases where you need to re-render your component after each state update or updating one state depends on another state variable. Considering this situation, React introduced `flushSync` method from `react-dom` API for the usecases where you need to flush state updates to DOM immediately.

The usage of `flushSync` method within an `onClick` event handler will be looking like as below,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { flushSync } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">handleClick</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-title function_">flushSync</span>(<span class="hljs-function">() =></span> {
        <span class="hljs-title function_">setClicked</span>(!clicked); <span class="hljs-comment">//Component will create a re-render here</span>
    });
    <span class="hljs-title function_">setCount</span>(count + <span class="hljs-number">1</span>); <span class="hljs-comment">// Component will create a re-render again here</span>
};
</code></pre>
<!-- codeblock-end -->

In the above click handler, React will update DOM at first using flushSync and second time updates DOM because of the counter setter function by avoiding automatic batching.

========== Id ==========  
254

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#254-Is-it-possible-to-prevent-automatic-batchi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
