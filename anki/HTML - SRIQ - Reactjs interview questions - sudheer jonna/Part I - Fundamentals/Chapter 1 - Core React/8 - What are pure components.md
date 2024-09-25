========== Question ==========  

### What are Pure Components?  

========== Answer ==========  

Pure components are the components which render the same output for the same state and props. In function components, you can achieve these pure components through memoized `React.memo()` API wrapping around the component. This API prevents unnecessary re-renders by comparing the previous props and new props using shallow comparison. So it will be helpful for performance optimizations.

But at the same time, it won't compare the previous state with the current state because function component itself prevents the unnecessary rendering by default when you set the same state again.

The syntactic representation of memoized components looks like below,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MemoizedComponent</span> = <span class="hljs-title function_">memo</span>(<span class="hljs-title class_">SomeComponent</span>, arePropsEqual?);
</code></pre>
<!-- codeblock-end -->

Below is the example of how child component(i.e., EmployeeProfile) prevents re-renders for the same props passed by parent component(i.e.,EmployeeRegForm).

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { memo, useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title class_">EmployeeProfile</span> = <span class="hljs-title function_">memo</span>(<span class="hljs-keyword">function</span> <span class="hljs-title function_">EmployeeProfile</span>(<span class="hljs-params">{ name, email }</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>Name:{name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>Email: {email}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
});
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">EmployeeRegForm</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [name, setName] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">''</span>);
    <span class="hljs-keyword">const</span> [email, setEmail] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">''</span>);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Name: <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{name}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{(e)</span> =></span> setName(e.target.value)} />
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Email: <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{email}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{(e)</span> =></span> setEmail(e.target.value)} />
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">hr</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">EmployeeProfile</span> <span class="hljs-attr">name</span>=<span class="hljs-string">{name}</span> /></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

In the above code, the email prop has not been passed to child component. So there won't be any re-renders for email prop change.

In class components, the components extending _`React.PureComponent`_ instead of _`React.Component`_ become the pure components. When props or state changes, _PureComponent_ will do a shallow comparison on both props and state by invoking `shouldComponentUpdate()` lifecycle method.

**Note:** `React.memo()` is a higher-order component.

========== Id ==========  
8

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#8-What-are-pure-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
