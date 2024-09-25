========== Question ==========  

### What is children prop?  

========== Answer ==========  

_Children_ is a prop that allows you to pass components as data to other components, just like any other prop you use. Component tree put between component's opening and closing tag will be passed to that component as `children` prop.

A simple usage of children prop looks as below,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">MyDiv</span>(<span class="hljs-params">{ children }</span>){
    <span class="hljs-keyword">return</span> (
      <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
        {children}
      <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    );
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Greeting</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyDiv</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>{"Hello"}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>{"World"}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">MyDiv</span>></span></span>
  );
}
</code></pre>
<!-- codeblock-end -->

<details><summary><b>See Class</b></summary>

<p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MyDiv</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createClass</span>({
    <span class="hljs-attr">render</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{this.props.children}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    },
});
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyDiv</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>{'Hello'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>{'World'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">MyDiv</span>></span></span>,
    node,
);
</code></pre>
<!-- codeblock-end -->

</p>

</details>

**Note:** There are several methods available in the legacy React API to work with this prop. These include `React.Children.map`, `React.Children.forEach`, `React.Children.count`, `React.Children.only`, `React.Children.toArray`.

========== Id ==========  
26

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#26-What-is-children-prop

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
