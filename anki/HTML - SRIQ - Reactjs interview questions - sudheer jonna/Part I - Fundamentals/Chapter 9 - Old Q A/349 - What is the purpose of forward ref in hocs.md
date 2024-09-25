========== Question ==========  

### What is the purpose of forward ref in HOCs?  

========== Answer ==========  

Refs will not get passed through because ref is not a prop. It is handled differently by React just like **key**. If you add a ref to a HOC, the ref will refer to the outermost container component, not the wrapped component. In this case, you can use Forward Ref API. For example, we can explicitly forward refs to the inner FancyButton component using the React.forwardRef API.

The below HOC logs all props,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">logProps</span>(<span class="hljs-params">Component</span>) {
    <span class="hljs-keyword">class</span> <span class="hljs-title class_">LogProps</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
        <span class="hljs-title function_">componentDidUpdate</span>(<span class="hljs-params">prevProps</span>) {
            <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'old props:'</span>, prevProps);
            <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'new props:'</span>, <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>);
        }
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">const</span> { forwardedRef, ...rest } = <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>;
            <span class="hljs-comment">// Assign the custom prop "forwardedRef" as a ref</span>
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Component</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{forwardedRef}</span> {<span class="hljs-attr">...rest</span>} /></span></span>;
        }
    }
    <span class="hljs-keyword">return</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">forwardRef</span>(<span class="hljs-function">(<span class="hljs-params">props, ref</span>) =></span> {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">LogProps</span> {<span class="hljs-attr">...props</span>} <span class="hljs-attr">forwardedRef</span>=<span class="hljs-string">{ref}</span> /></span></span>;
    });
}
</code></pre>
<!-- codeblock-end -->

Let's use this HOC to log all props that get passed to our “fancy button” component,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">FancyButton</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">focus</span>(<span class="hljs-params"></span>) {
        <span class="hljs-comment">// ...</span>
    }
    <span class="hljs-comment">// ...</span>
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">logProps</span>(<span class="hljs-title class_">FancyButton</span>);
</code></pre>
<!-- codeblock-end -->

Now let's create a ref and pass it to FancyButton component. In this case, you can set focus to button element.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">FancyButton</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./FancyButton'</span>;
<span class="hljs-keyword">const</span> ref = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createRef</span>();
ref.<span class="hljs-property">current</span>.<span class="hljs-title function_">focus</span>();
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">FancyButton</span> <span class="hljs-attr">label</span>=<span class="hljs-string">'Click Me'</span> <span class="hljs-attr">handleClick</span>=<span class="hljs-string">{handleClick}</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{ref}</span> /></span></span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
349

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#349-What-is-the-purpose-of-forward-ref-in-hocs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
