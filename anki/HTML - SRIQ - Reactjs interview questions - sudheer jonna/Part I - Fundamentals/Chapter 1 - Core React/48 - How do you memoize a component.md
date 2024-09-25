========== Question ==========  

### How do you memoize a component?  

========== Answer ==========  

There are memoize libraries available which can be used on function components.

For example `moize` library can memoize the component in another component.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> moize <span class="hljs-keyword">from</span> <span class="hljs-string">'moize'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">Component</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./components/Component'</span>; <span class="hljs-comment">// this module exports a non-memoized component</span>
<span class="hljs-keyword">const</span> <span class="hljs-title class_">MemoizedFoo</span> = moize.<span class="hljs-title function_">react</span>(<span class="hljs-title class_">Component</span>);
<span class="hljs-keyword">const</span> <span class="hljs-title function_">Consumer</span> = (<span class="hljs-params"></span>) => {
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
        {'I will memoize the following entry:'}
        <span class="hljs-tag">&#x3C;<span class="hljs-name">MemoizedFoo</span> /></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
};
</code></pre>
<!-- codeblock-end -->

**Update:** Since React v16.6.0, we have a `React.memo`. It provides a higher order component which memoizes component unless the props change. To use it, simply wrap the component using React.memo before you use it.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MemoComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">memo</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">MemoComponent</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-comment">/* render using props */</span>
});
<span class="hljs-variable constant_">OR</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">memo</span>(<span class="hljs-title class_">MyFunctionComponent</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
48

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#48-How-do-you-memoize-a-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
