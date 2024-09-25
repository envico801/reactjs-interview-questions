========== Question ==========  

### How to pass a parameter to an event handler or callback?  

========== Answer ==========  

You can use an _arrow function_ to wrap around an _event handler_ and pass parameters:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button onClick={<span class="hljs-function">() =></span> <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">handleClick</span>(id)} />
</code></pre>
<!-- codeblock-end -->

This is an equivalent to calling `.bind`:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button onClick={<span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>, id)} />
</code></pre>
<!-- codeblock-end -->

Apart from these two approaches, you can also pass arguments to a function which is defined as arrow function

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button onClick={<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">handleClick</span>(id)} />;
handleClick = <span class="hljs-function">(<span class="hljs-params">id</span>) =></span> <span class="hljs-function">() =></span> {
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Hello, your ticket number is'</span>, id);
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
274

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#274-How-to-pass-a-parameter-to-an-event-handle

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
