========== Question ==========  

### Why we need to pass a function to setState()?  

========== Answer ==========  

The reason behind for this is that `setState()` is an asynchronous operation. React batches state changes for performance reasons, so the state may not change immediately after `setState()` is called. That means you should not rely on the current state when calling `setState()` since you can't be sure what that state will be. The solution is to pass a function to `setState()`, with the previous state as an argument. By doing this you can avoid issues with the user getting the old state value on access due to the asynchronous nature of `setState()`.

Let's say the initial count value is zero. After three consecutive increment operations, the value is going to be incremented only by one.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// assuming this.state.count === 0</span>
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">count</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">count</span> + <span class="hljs-number">1</span> });
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">count</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">count</span> + <span class="hljs-number">1</span> });
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">count</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">count</span> + <span class="hljs-number">1</span> });
<span class="hljs-comment">// this.state.count === 1, not 3</span>
</code></pre>
<!-- codeblock-end -->

If we pass a function to `setState()`, the count gets incremented correctly.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">prevState, props</span>) =></span> ({
    <span class="hljs-attr">count</span>: prevState.<span class="hljs-property">count</span> + props.<span class="hljs-property">increment</span>,
}));
<span class="hljs-comment">// this.state.count === 3 as expected</span>
</code></pre>
<!-- codeblock-end -->

**(OR)**

### Why function is preferred over object for `setState()`?

React may batch multiple `setState()` calls into a single update for performance. Because `this.props` and `this.state` may be updated asynchronously, you should not rely on their values for calculating the next state.

This counter example will fail to update as expected:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Wrong</span>
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
    <span class="hljs-attr">counter</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">counter</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">increment</span>,
});
</code></pre>
<!-- codeblock-end -->

The preferred approach is to call `setState()` with function rather than object. That function will receive the previous state as the first argument, and the props at the time the update is applied as the second argument.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Correct</span>
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">prevState, props</span>) =></span> ({
    <span class="hljs-attr">counter</span>: prevState.<span class="hljs-property">counter</span> + props.<span class="hljs-property">increment</span>,
}));
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
301

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#301-Why-we-need-to-pass-a-function-to-setstate

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
