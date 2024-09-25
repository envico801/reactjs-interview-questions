========== Question ==========  

### Is it good to use `setState()` in `componentWillMount()` method?  

========== Answer ==========  

Yes, it is safe to use `setState()` inside `componentWillMount()` method. But at the same it is recommended to avoid async initialization in `componentWillMount()` lifecycle method. `componentWillMount()` is invoked immediately before mounting occurs. It is called before `render()`, therefore setting state in this method will not trigger a re-render. Avoid introducing any side-effects or subscriptions in this method. We need to make sure async calls for component initialization happened in `componentDidMount()` instead of `componentWillMount()`.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
  axios.<span class="hljs-title function_">get</span>(<span class="hljs-string">`api/todos`</span>)
    .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">result</span>) =></span> {
      <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
        <span class="hljs-attr">messages</span>: [...result.<span class="hljs-property">data</span>]
      })
    })
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
291

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#291-Is-it-good-to-use-setstate-in-compone

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
