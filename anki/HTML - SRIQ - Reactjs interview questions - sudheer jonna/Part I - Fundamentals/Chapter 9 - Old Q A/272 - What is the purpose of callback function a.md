========== Question ==========  

### What is the purpose of callback function as an argument of `setState()`?  

========== Answer ==========  

The callback function is invoked when setState finished and the component gets rendered. Since `setState()` is **asynchronous** the callback function is used for any post action.

**Note:** It is recommended to use lifecycle method rather than this callback function.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">setState</span>({ <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span> }, <span class="hljs-function">() =></span> <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'The name has updated and component re-rendered'</span>));
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
272

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#272-What-is-the-purpose-of-callback-function-a

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
