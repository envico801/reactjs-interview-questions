========== Question ==========  

### How do you conditionally render components?  

========== Answer ==========  

In some cases you want to render different components depending on some state. JSX does not render `false` or `undefined`, so you can use conditional _short-circuiting_ to render a given part of your component only if a certain condition is true.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">MyComponent</span> = (<span class="hljs-params">{ name, address }</span>) => (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
        {address &#x26;&#x26; <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{address}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>}
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
);
</code></pre>
<!-- codeblock-end -->

If you need an `if-else` condition then use _ternary operator_.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">MyComponent</span> = (<span class="hljs-params">{ name, address }</span>) => (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
        {address ?
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{address}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        :   <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{'Address is not available'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>}
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
46

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#46-How-do-you-conditionally-render-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
