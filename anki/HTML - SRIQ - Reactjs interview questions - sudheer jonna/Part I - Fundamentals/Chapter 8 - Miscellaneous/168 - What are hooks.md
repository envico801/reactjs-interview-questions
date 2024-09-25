========== Question ==========  

### What are hooks?  

========== Answer ==========  

Hooks is a special JavaScript function that allows you use state and other React features without writing a class. This pattern has been introduced as a new feature in React 16.8 and helped to isolate the stateful logic from the components.

Let's see an example of useState hook:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">Example</span>(<span class="hljs-params"></span>) {
    <span class="hljs-comment">// Declare a new state variable, which we'll call "count"</span>
    <span class="hljs-keyword">const</span> [count, setCount] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">0</span>);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>You clicked {count} times<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> setCount(count + 1)}>Click me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

**Note:** Hooks can be used inside an existing function component without rewriting the component.

========== Id ==========  
168

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#168-What-are-hooks

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
