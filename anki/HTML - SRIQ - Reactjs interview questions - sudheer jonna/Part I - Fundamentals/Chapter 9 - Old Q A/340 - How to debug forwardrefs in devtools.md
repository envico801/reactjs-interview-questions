========== Question ==========  

### How to debug forwardRefs in DevTools?  

========== Answer ==========  

**React.forwardRef** accepts a render function as parameter and DevTools uses this function to determine what to display for the ref forwarding component.

For example, If you don't name the render function or not using displayName property then it will appear as ”ForwardRef” in the DevTools,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">WrappedComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>(<span class="hljs-function">(<span class="hljs-params">props, ref</span>) =></span> {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">LogProps</span> {<span class="hljs-attr">...props</span>} <span class="hljs-attr">forwardedRef</span>=<span class="hljs-string">{ref}</span> /></span></span>;
});
</code></pre>
<!-- codeblock-end -->

But If you name the render function then it will appear as **”ForwardRef(myFunction)”**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">WrappedComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">myFunction</span>(<span class="hljs-params">props, ref</span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">LogProps</span> {<span class="hljs-attr">...props</span>} <span class="hljs-attr">forwardedRef</span>=<span class="hljs-string">{ref}</span> /></span></span>;
});
</code></pre>
<!-- codeblock-end -->

As an alternative, You can also set displayName property for forwardRef function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">logProps</span>(<span class="hljs-params">Component</span>) {
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">LogProps</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
        <span class="hljs-comment">// ...</span>
    }
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">forwardRef</span>(<span class="hljs-params">props, ref</span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">LogProps</span> {<span class="hljs-attr">...props</span>} <span class="hljs-attr">forwardedRef</span>=<span class="hljs-string">{ref}</span> /></span></span>;
    }
    <span class="hljs-comment">// Give this component a more helpful display name in DevTools.</span>
    <span class="hljs-comment">// e.g. "ForwardRef(logProps(MyComponent))"</span>
    <span class="hljs-keyword">const</span> name = <span class="hljs-title class_">Component</span>.<span class="hljs-property">displayName</span> || <span class="hljs-title class_">Component</span>.<span class="hljs-property">name</span>;
    forwardRef.<span class="hljs-property">displayName</span> = <span class="hljs-string">`logProps(<span class="hljs-subst">${name}</span>)`</span>;
    <span class="hljs-keyword">return</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>(forwardRef);
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
340

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#340-How-to-debug-forwardrefs-in-devtools

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
