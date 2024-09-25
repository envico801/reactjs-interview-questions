========== Question ==========  

### How does React batch multiple state updates?  

========== Answer ==========  

React prevents component from re-rendering for each and every state update by grouping multiple state updates within an event handler. This strategy improves the application performance and this process known as **batching**. The older version of React only supported batching for browser events whereas React18 supported for asynchronous actions, timeouts and intervals along with native events. This improved version of batching is called **automatic batching**.

Let's demonstrate this automatic batching feature with a below example.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">BatchingState</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [count, setCount] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">0</span>);
    <span class="hljs-keyword">const</span> [message, setMessage] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'batching'</span>);
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Application Rendered'</span>);
    <span class="hljs-keyword">const</span> <span class="hljs-title function_">handleUsers</span> = (<span class="hljs-params"></span>) => {
        <span class="hljs-title function_">fetch</span>(<span class="hljs-string">'https://jsonplaceholder.typicode.com/users/1'</span>).<span class="hljs-title function_">then</span>(<span class="hljs-function">() =></span> {
            <span class="hljs-comment">// Automatic Batching re-render only once</span>
            <span class="hljs-title function_">setCount</span>(count + <span class="hljs-number">1</span>);
            <span class="hljs-title function_">setMessage</span>(<span class="hljs-string">'users fetched'</span>);
        });
    };
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{count}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleAsyncFetch}</span>></span>Click Me!<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

The preceding code updated two state variables with in an event handler. However, React will perform automatic batching feature and the component will be re-rendered only once for better performance.

========== Id ==========  
253

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#253-How-does-react-batch-multiple-state-update

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
