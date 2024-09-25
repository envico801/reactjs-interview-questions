========== Question ==========  

### What are forward refs?  

========== Answer ==========  

_Ref forwarding_ is a feature that lets some components take a _ref_ they receive, and pass it further down to a child.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title class_">ButtonElement</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>(<span class="hljs-function">(<span class="hljs-params">props, ref</span>) =></span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{ref}</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'CustomButton'</span>></span>
        {props.children}
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
));
<span class="hljs-comment">// Create ref to the DOM button:</span>
<span class="hljs-keyword">const</span> ref = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createRef</span>();
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ButtonElement</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{ref}</span>></span>{'Forward Ref'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">ButtonElement</span>></span></span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
277

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#277-What-are-forward-refs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
