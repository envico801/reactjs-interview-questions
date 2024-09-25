========== Question ==========  

### What is Shallow Renderer in React testing?  

========== Answer ==========  

_Shallow rendering_ is useful for writing unit test cases in React. It lets you render a component _one level deep_ and assert facts about what its render method returns, without worrying about the behavior of child components, which are not instantiated or rendered.

For example, if you have the following component:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">MyComponent</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">heading</span>'}></span>{'Title'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">description</span>'}></span>{'Description'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

Then you can assert as follows:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">ShallowRenderer</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-test-renderer/shallow'</span>;
<span class="hljs-comment">// in your test</span>
<span class="hljs-keyword">const</span> renderer = <span class="hljs-keyword">new</span> <span class="hljs-title class_">ShallowRenderer</span>();
renderer.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyComponent</span> /></span></span>);
<span class="hljs-keyword">const</span> result = renderer.<span class="hljs-title function_">getRenderOutput</span>();
<span class="hljs-title function_">expect</span>(result.<span class="hljs-property">type</span>).<span class="hljs-title function_">toBe</span>(<span class="hljs-string">'div'</span>);
<span class="hljs-title function_">expect</span>(result.<span class="hljs-property">props</span>.<span class="hljs-property">children</span>).<span class="hljs-title function_">toEqual</span>([<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">span</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">heading</span>'}></span>{'Title'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span></span>, <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">span</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">description</span>'}></span>{'Description'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span></span>]);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
96

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 4 - React Testing

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-4-React-Testing::#96-What-is-shallow-renderer-in-react-testing

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
