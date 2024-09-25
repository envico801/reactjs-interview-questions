========== Question ==========  

### What is the difference between `super()` and `super(props)` in React using ES6 classes?  

========== Answer ==========  

When you want to access `this.props` in `constructor()` then you should pass props to `super()` method.

**Using `super(props)`:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>); <span class="hljs-comment">// { name: 'John', ... }</span>
    }
}
</code></pre>
<!-- codeblock-end -->

**Using `super()`:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>();
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>); <span class="hljs-comment">// undefined</span>
    }
}
</code></pre>
<!-- codeblock-end -->

Outside `constructor()` both will display same value for `this.props`.

========== Id ==========  
305

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#305-What-is-the-difference-between-super-a

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
