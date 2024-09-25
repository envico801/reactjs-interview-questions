========== Question ==========  

### Does the lazy function support named exports?  

========== Answer ==========  

No, currently `React.lazy` function supports default exports only. If you would like to import modules which are named exports, you can create an intermediate module that reexports it as the default. It also ensures that tree shaking keeps working and don’t pull unused components.

Let's take a component file which exports multiple named components,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// MoreComponents.js</span>
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-title class_">SomeComponent</span> = <span class="hljs-comment">/* ... */</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-title class_">UnusedComponent</span> = <span class="hljs-comment">/* ... */</span>;
</code></pre>
<!-- codeblock-end -->

and reexport `MoreComponents.js` components in an intermediate file `IntermediateComponent.js`

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// IntermediateComponent.js</span>
<span class="hljs-keyword">export</span> { <span class="hljs-title class_">SomeComponent</span> <span class="hljs-keyword">as</span> <span class="hljs-keyword">default</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./MoreComponents.js'</span>;
</code></pre>
<!-- codeblock-end -->

Now you can import the module using lazy function as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { lazy } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title class_">SomeComponent</span> = <span class="hljs-title function_">lazy</span>(<span class="hljs-function">() =></span> <span class="hljs-keyword">import</span>(<span class="hljs-string">'./IntermediateComponent.js'</span>));
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
29

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#29-Does-the-lazy-function-support-named-expor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
