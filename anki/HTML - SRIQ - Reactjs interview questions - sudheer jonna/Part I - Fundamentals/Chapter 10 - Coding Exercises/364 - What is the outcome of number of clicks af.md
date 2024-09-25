========== Question ==========  

### What is the outcome of number of clicks after 3 button clicks?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { useRef } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Counter</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">let</span> ref = <span class="hljs-title function_">useRef</span>(<span class="hljs-number">0</span>);
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
        ref.<span class="hljs-property">current</span> = ref.<span class="hljs-property">current</span> + <span class="hljs-number">1</span>;
    }
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>Clicked + {ref.current} + times<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleClick}</span>></span>Click me!<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

-   1: 3 times

-   2: 4 times

-   3: 2 times

-   4: 0 times  

========== Answer ==========  

Answer: 4

If you try to use **{ref.current}** in the render method, the number won’t be updated on click. This is because **ref.current** does not trigger a re-render unlike state. This property is mainly used to read and write the values inside event handler or outside the render method.

========== Id ==========  
364

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 10 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-10-Coding-Exercises::#364-What-is-the-outcome-of-number-of-clicks-af

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
