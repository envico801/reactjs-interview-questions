========== Question ==========  

### How to bind methods or event handlers in JSX callbacks?  

========== Answer ==========  

There are 3 possible ways to achieve this in class components:

1. **Binding in Constructor:** In JavaScript classes, the methods are not bound by default. The same rule applies for React event handlers defined as class methods. Normally we bind them in constructor.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span> = <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
    }
    <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'SingOut triggered'</span>);
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick}</span>></span>SingOut<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

2. **Public class fields syntax:** If you don't like to use bind approach then _public class fields syntax_ can be used to correctly bind callbacks. The Create React App enables this syntax by default.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">handleClick = <span class="hljs-function">() =></span> {
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'SingOut triggered'</span>, <span class="hljs-variable language_">this</span>);
};
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button onClick={<span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span>}><span class="hljs-title class_">SingOut</span>&#x3C;/button>
</code></pre>
<!-- codeblock-end -->

3. **Arrow functions in callbacks:** It is possible to use _arrow functions_ directly in the callbacks.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
    <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'SingOut triggered'</span>);
}
<span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> this.handleClick()}>SignOut<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

**Note:** If the callback is passed as prop to child components, those components might do an extra re-rendering. In those cases, it is preferred to go with `.bind()` or _public class fields syntax_ approach considering performance.

========== Id ==========  
273

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#273-How-to-bind-methods-or-event-handlers-in-j

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
