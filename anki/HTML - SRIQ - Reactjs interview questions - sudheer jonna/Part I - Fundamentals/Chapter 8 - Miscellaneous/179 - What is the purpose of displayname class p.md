========== Question ==========  

### What is the purpose of displayName class property?  

========== Answer ==========  

The displayName string is used in debugging messages. Usually, you don’t need to set it explicitly because it’s inferred from the name of the function or class that defines the component. You might want to set it explicitly if you want to display a different name for debugging purposes or when you create a higher-order component.

For example, To ease debugging, choose a display name that communicates that it’s the result of a withSubscription HOC.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">withSubscription</span>(<span class="hljs-params">WrappedComponent</span>) {
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">WithSubscription</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
        <span class="hljs-comment">/* ... */</span>
    }
    <span class="hljs-title class_">WithSubscription</span>.<span class="hljs-property">displayName</span> = <span class="hljs-string">`WithSubscription(<span class="hljs-subst">${getDisplayName(WrappedComponent)}</span>)`</span>;
    <span class="hljs-keyword">return</span> <span class="hljs-title class_">WithSubscription</span>;
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">getDisplayName</span>(<span class="hljs-params">WrappedComponent</span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-title class_">WrappedComponent</span>.<span class="hljs-property">displayName</span> || <span class="hljs-title class_">WrappedComponent</span>.<span class="hljs-property">name</span> || <span class="hljs-string">'Component'</span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
179

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#179-What-is-the-purpose-of-displayname-class-p

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
