========== Question ==========  

### What is the difference between Element and Component?  

========== Answer ==========  

An _Element_ is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. _Elements_ can contain other _Elements_ in their props. Creating a React element is cheap. Once an element is created, it cannot be mutated.

The JavaScript representation(Without JSX) of React Element would be as follows:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> element = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'div'</span>, { <span class="hljs-attr">id</span>: <span class="hljs-string">'login-btn'</span> }, <span class="hljs-string">'Login'</span>);
</code></pre>
<!-- codeblock-end -->

and this element can be simiplified using JSX

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">id</span>=<span class="hljs-string">"login-btn"</span>></span>Login<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
</code></pre>
<!-- codeblock-end -->

The above `React.createElement()` function returns an object as below:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">{
  <span class="hljs-attr">type</span>: <span class="hljs-string">'div'</span>,
  <span class="hljs-attr">props</span>: {
    <span class="hljs-attr">children</span>: <span class="hljs-string">'Login'</span>,
    <span class="hljs-attr">id</span>: <span class="hljs-string">'login-btn'</span>
  }
}
</code></pre>
<!-- codeblock-end -->

Finally, this element renders to the DOM using `ReactDOM.render()`.

Whereas a **component** can be declared in several different ways. It can be a class with a `render()` method or it can be defined as a function. In either case, it takes props as an input, and returns a JSX tree as the output:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">Button</span> = (<span class="hljs-params">{ handleLogin }</span>) => (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">id</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">login-btn</span>'} <span class="hljs-attr">onClick</span>=<span class="hljs-string">{handleLogin}</span>></span>
        Login
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
);
</code></pre>
<!-- codeblock-end -->

Then JSX gets transpiled to a `React.createElement()` function tree:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">Button</span> = (<span class="hljs-params">{ handleLogin }</span>) => <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'div'</span>, { <span class="hljs-attr">id</span>: <span class="hljs-string">'login-btn'</span>, <span class="hljs-attr">onClick</span>: handleLogin }, <span class="hljs-string">'Login'</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
5

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#5-What-is-the-difference-between-element-and

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
