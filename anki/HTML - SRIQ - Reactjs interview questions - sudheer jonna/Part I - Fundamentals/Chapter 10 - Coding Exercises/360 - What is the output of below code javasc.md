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
                    setCounter(counter + 5);
                    setCounter(counter + 5);
                    alert(counter);
                    setCounter(counter + 5);
                    setCounter(counter + 5);
                }}
            >
                Increment
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

-   1: Alert with 5, 5

-   2: Alert with 15, 25

-   3: Alert with 5, 10

-   4: Error: Cannot update the same state multiple times concurrently  

========== Answer ==========  

Answer: 3

State values are fixed(i.e, default value 5) in each render and setting the state only changes it for the next render. React will wait until all the code executed with in an event handler before your state updates followed by re-rendering the UI. Also, all the 3 setter function calls are replacing the calculated value. Hence, irrespective of how many times you call `setCounter(counter + 5)` the final value is 10(5+5).

This can be visuallized by substituting with state variable values in the particular render,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;button
    onClick={<span class="hljs-function">() =></span> {
        <span class="hljs-title function_">setCounter</span>(<span class="hljs-number">5</span> + <span class="hljs-number">5</span>);
        <span class="hljs-title function_">setCounter</span>(<span class="hljs-number">5</span> + <span class="hljs-number">5</span>);
        <span class="hljs-title function_">alert</span>(<span class="hljs-number">5</span>);
        <span class="hljs-title function_">setCounter</span>(<span class="hljs-number">5</span> + <span class="hljs-number">5</span>);
        <span class="hljs-title function_">setCounter</span>(<span class="hljs-number">5</span> + <span class="hljs-number">5</span>);
    }}
>
    <span class="hljs-title class_">Increment</span>
&#x3C;/button>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
360

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 10 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-10-Coding-Exercises::#360-What-is-the-output-of-below-code-javasc

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
