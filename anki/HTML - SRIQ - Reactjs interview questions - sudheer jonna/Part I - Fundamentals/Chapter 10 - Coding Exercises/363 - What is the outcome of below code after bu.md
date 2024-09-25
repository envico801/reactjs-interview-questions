========== Question ==========  

### What is the outcome of below code after button click?

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { useRef } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">MyCustomInput</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> {<span class="hljs-attr">...props</span>} /></span></span>;
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">MyCustomForm</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> inputRef = <span class="hljs-title function_">useRef</span>(<span class="hljs-literal">null</span>);
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleInputFocus</span>(<span class="hljs-params"></span>) {
        inputRef.<span class="hljs-property">current</span>.<span class="hljs-title function_">focus</span>();
    }
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">MyCustomInput</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{inputRef}</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleInputFocus}</span>></span>Click Me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

-   1: Input gets the focus

-   2: Warning: Function components cannot be given refs.

-   3: Cannot read current property of undefined

-   4: Warning: Missing ref on `<input />` element  

========== Answer ==========  

Answer: 2

By default, React does not allow a component access the DOM nodes of other components even for child components. If you still try to access the DOM nodes directly then you will receive below error:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Warning</span>: <span class="hljs-title class_">Function</span> components cannot be given refs. <span class="hljs-title class_">Attempts</span> to access <span class="hljs-variable language_">this</span> ref will fail. <span class="hljs-title class_">Did</span> you mean to use <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>()?
</code></pre>
<!-- codeblock-end -->

This issue can be fixed by wrapping the **`<MyCustomInput />`** component with `forwardRef` function which accepts ref as the second argument which can be used on the **`<input />`** element as **ref={ref}**

========== Id ==========  
363

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 10 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-10-Coding-Exercises::#363-What-is-the-outcome-of-below-code-after-bu

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
