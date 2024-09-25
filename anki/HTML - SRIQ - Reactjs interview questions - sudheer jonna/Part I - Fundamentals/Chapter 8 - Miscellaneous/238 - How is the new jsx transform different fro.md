========== Question ==========  

### How is the new JSX transform different from old transform??  

========== Answer ==========  

The new JSX transform doesn’t require React to be in scope. i.e, You don't need to import React package for simple scenarios.

Let's take an example to look at the main differences between the old and the new transform,

**Old Transform:**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Good morning!!<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

Now JSX transform convert the above code into regular JavaScript as below,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'h1'</span>, <span class="hljs-literal">null</span>, <span class="hljs-string">'Good morning!!'</span>);
}
</code></pre>
<!-- codeblock-end -->

**New Transform:**

The new JSX transform doesn't require any React imports

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Good morning!!<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

Under the hood JSX transform compiles to below code

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">import</span> { jsx <span class="hljs-keyword">as</span> _jsx } <span class="hljs-keyword">from</span> <span class="hljs-string">'react/jsx-runtime'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-title function_">_jsx</span>(<span class="hljs-string">'h1'</span>, { <span class="hljs-attr">children</span>: <span class="hljs-string">'Good morning!!'</span> });
}
</code></pre>
<!-- codeblock-end -->

**Note:** You still need to import React to use Hooks.

========== Id ==========  
238

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#238-How-is-the-new-jsx-transform-different-fro

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
