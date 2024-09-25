========== Question ==========  

### How to focus an input element on page load?  

========== Answer ==========  

You need to use `useEffect` hook to set focus on input field during page load time for functional component.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { useEffect, useRef } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">App</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">const</span> inputElRef = <span class="hljs-title function_">useRef</span>(<span class="hljs-literal">null</span>);
    <span class="hljs-title function_">useEffect</span>(<span class="hljs-function">() =></span> {
        inputElRef.<span class="hljs-property">current</span>.<span class="hljs-title function_">focus</span>();
    }, []);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">defaultValue</span>=<span class="hljs-string">{</span>"<span class="hljs-attr">Won</span>'<span class="hljs-attr">t</span> <span class="hljs-attr">focus</span>"} /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{inputElRef}</span> <span class="hljs-attr">defaultValue</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">Will</span> <span class="hljs-attr">focus</span>'} /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'app'</span>));
</code></pre>
<!-- codeblock-end -->

  <details><summary><b>See Class</b></summary>

  <p>

You can do it by creating _ref_ for `input` element and using it in `componentDidMount()`:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">nameInput</span>.<span class="hljs-title function_">focus</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">defaultValue</span>=<span class="hljs-string">{</span>"<span class="hljs-attr">Won</span>'<span class="hljs-attr">t</span> <span class="hljs-attr">focus</span>"} /></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{(input)</span> =></span> (this.nameInput = input)} defaultValue={'Will focus'} />
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'app'</span>));
</code></pre>
<!-- codeblock-end -->

  </p>

  </details>

========== Id ==========  
68

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#68-How-to-focus-an-input-element-on-page-load

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
