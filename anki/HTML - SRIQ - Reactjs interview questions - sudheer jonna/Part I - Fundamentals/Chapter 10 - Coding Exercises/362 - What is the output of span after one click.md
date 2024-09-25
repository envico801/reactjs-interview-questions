========== Question ==========  

### What is the output of span after one click?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { useRef } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Counter</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">let</span> countRef = <span class="hljs-title function_">useRef</span>(<span class="hljs-number">0</span>);
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleIncrement</span>(<span class="hljs-params"></span>) {
        countRef.<span class="hljs-property">current</span> = countRef.<span class="hljs-property">current</span> + <span class="hljs-number">1</span>;
    }
    <span class="hljs-keyword">return</span>;
    <span class="xml"><span class="hljs-tag">&#x3C;></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>Count: {countRef.current}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleIncrement}</span>></span>Click me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
    <span class="hljs-tag">&#x3C;/></span></span>;
}
</code></pre>
<!-- codeblock-end -->

-   1: Cannot read current property of undefined

-   2: Count: 1

-   3: null

-   4: Count: 0  

========== Answer ==========  

Answer: 4

In React, every update has two phases.

1. **Render:** This is where React calls the components in order to output something on the screen

2. **Commit:** React applies changes to the DOM

Any updates to the ref will be reflected only in the commit phase. In other words, React sets **counterRef.current** during the commit phase. Hence, **countRef.current** always holds value `0` irrespective of how many times the Increment button clicked.

========== Id ==========  
362

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 10 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-10-Coding-Exercises::#362-What-is-the-output-of-span-after-one-click

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
