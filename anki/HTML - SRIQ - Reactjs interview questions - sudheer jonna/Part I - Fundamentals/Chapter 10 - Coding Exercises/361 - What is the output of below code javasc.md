========== Question ==========  

### What is the output of below code

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Counter</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [counter, setCounter] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">5</span>);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>{counter}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
                <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> {
                    setCounter((counter) => counter + 5);
                    setCounter((counter) => counter + 5);
                    alert(counter);
                    setCounter((counter) => counter + 5);
                    setCounter((counter) => counter + 5);
                }}
            >
                Increment
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

-   1: Alert with 5, 25

-   2: Alert with 5, 10

-   3: Alert with 15, 25

-   4: Alert with 15, 10  

========== Answer ==========  

Answer: 1

React queues all the updater functions(e.g, counter => counter + 5) which will be processed after all the code inside event handler has been executed. During the next re-render(state update through setState), React goes through the queue and increment the counter based on the previous value in each function call. So the final value of counter becomes 25(initial value 5 + 5 + 5 + 5 + 5) whereas the alert shows default value 5 because the counter value won't be updated by that time.

========== Id ==========  
361

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 10 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-10-Coding-Exercises::#361-What-is-the-output-of-below-code-javasc

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
