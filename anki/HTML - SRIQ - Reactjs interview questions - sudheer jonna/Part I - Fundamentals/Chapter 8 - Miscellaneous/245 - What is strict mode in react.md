========== Question ==========  

### What is strict mode in React?  

========== Answer ==========  

`React.StrictMode` is a useful component for highlighting potential problems in an application. Just like `<Fragment>`, `<StrictMode>` does not render any extra DOM elements. It activates additional checks and warnings for its descendants. These checks apply for _development mode_ only.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">StrictMode</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Header</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">StrictMode</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">ComponentOne</span> /></span>
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">ComponentTwo</span> /></span>
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">StrictMode</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Header</span> /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

In the example above, the _strict mode_ checks apply to `<ComponentOne>` and `<ComponentTwo>` components only. i.e., Part of the application only.

**Note:** Frameworks such as NextJS has this flag enabled by default.

========== Id ==========  
245

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#245-What-is-strict-mode-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
