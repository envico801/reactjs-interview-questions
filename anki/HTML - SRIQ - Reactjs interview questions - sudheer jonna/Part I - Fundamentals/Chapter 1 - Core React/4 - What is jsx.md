========== Question ==========  

### What is JSX?  

========== Answer ==========  

_JSX_ stands for _JavaScript XML_ and it is an XML-like syntax extension to ECMAScript. Basically it just provides the syntactic sugar for the `React.createElement(type, props, ...children)` function, giving us expressiveness of JavaScript along with HTML like template syntax.

In the example below, the text inside `<h1>` tag is returned as JavaScript function to the render function.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'greeting'</span>></span>{'Hello, this is a JSX Code!'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

If you don't use JSX syntax then the respective JavaScript code should be written as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { createElement } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="hljs-title function_">createElement</span>(<span class="hljs-string">'h1'</span>, { <span class="hljs-attr">className</span>: <span class="hljs-string">'greeting'</span> }, <span class="hljs-string">'Hello, this is a JSX Code!'</span>);
}
</code></pre>
<!-- codeblock-end -->

 <details><summary><b>See Class</b></summary>

 <p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'greeting'</span>></span>{'Hello, this is a JSX Code!'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

 </p>

 </details>

**Note:** JSX is stricter than HTML

========== Id ==========  
4

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#4-What-is-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
