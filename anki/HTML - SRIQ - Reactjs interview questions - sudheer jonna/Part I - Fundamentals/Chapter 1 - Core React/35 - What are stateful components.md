========== Question ==========  

### What are stateful components?  

========== Answer ==========  

If the behaviour of a component is dependent on the _state_ of the component then it can be termed as stateful component. These _stateful components_ are either function components with hooks or _class components_.

Let's take an example of function stateful component which update the state based on click event,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, {useState} <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">App</span> = (<span class="hljs-params">props</span>) => {
<span class="hljs-keyword">const</span> [count, setCount] = <span class="hljs-title function_">useState</span>(<span class="hljs-number">0</span>);
<span class="hljs-title function_">handleIncrement</span>(<span class="hljs-params"></span>) {
  <span class="hljs-title function_">setCount</span>(count+<span class="hljs-number">1</span>);
}
<span class="hljs-keyword">return</span> (
  <span class="xml"><span class="hljs-tag">&#x3C;></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleIncrement}</span>></span>Increment<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
    <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>Counter: {count}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
  <span class="hljs-tag">&#x3C;/></span></span>
  )
}
</code></pre>
<!-- codeblock-end -->

<details><summary><b>See Class</b></summary>

<p>

The equivalent class stateful component with a state that gets initialized in the `constructor`.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">count</span>: <span class="hljs-number">0</span> };
    }
    <span class="hljs-title function_">handleIncrement</span>(<span class="hljs-params"></span>) {
        <span class="hljs-title function_">setState</span>({ <span class="hljs-attr">count</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">count</span> + <span class="hljs-number">1</span> });
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> this.handleIncrement}>Increment<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>Count: {count}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

</p>

</details>

========== Id ==========  
35

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#35-What-are-stateful-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
