========== Question ==========  

### Why should we not update the state directly?  

========== Answer ==========  

If you try to update the state directly then it won't re-render the component.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Wrong</span>
<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">message</span> = <span class="hljs-string">'Hello world'</span>;
</code></pre>
<!-- codeblock-end -->

Instead use `setState()` method. It schedules an update to a component's state object. When state changes, the component responds by re-rendering.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Correct</span>
<span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">message</span>: <span class="hljs-string">'Hello World'</span> });
</code></pre>
<!-- codeblock-end -->

**Note:** You can directly assign to the state object either in _constructor_ or using latest javascript's class field declaration syntax.

========== Id ==========  
271

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#271-Why-should-we-not-update-the-state-directl

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
