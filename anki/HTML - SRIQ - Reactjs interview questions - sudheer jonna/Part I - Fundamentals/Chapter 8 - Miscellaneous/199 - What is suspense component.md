========== Question ==========  

### What is suspense component?  

========== Answer ==========  

If the module containing the dynamic import is not yet loaded by the time parent component renders, you must show some fallback content while you’re waiting for it to load using a loading indicator. This can be done using **Suspense** component.

For example, the below code uses suspense component,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">OtherComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">lazy</span>(<span class="hljs-function">() =></span> <span class="hljs-keyword">import</span>(<span class="hljs-string">'./OtherComponent'</span>));
<span class="hljs-keyword">function</span> <span class="hljs-title function_">MyComponent</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Suspense</span> <span class="hljs-attr">fallback</span>=<span class="hljs-string">{</span>&#x3C;<span class="hljs-attr">div</span>></span>Loading...<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>}>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">OtherComponent</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">Suspense</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

As mentioned in the above code, Suspense is wrapped above the lazy component.

========== Id ==========  
199

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#199-What-is-suspense-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
