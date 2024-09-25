========== Question ==========  

### What is the purpose of using super constructor with props argument?  

========== Answer ==========  

A child class constructor cannot make use of `this` reference until the `super()` method has been called. The same applies to ES6 sub-classes as well. The main reason for passing props parameter to `super()` call is to access `this.props` in your child constructors.

**Passing props:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>); <span class="hljs-comment">// prints { name: 'John', age: 42 }</span>
    }
}
</code></pre>
<!-- codeblock-end -->

**Not passing props:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>();
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>); <span class="hljs-comment">// prints undefined</span>
        <span class="hljs-comment">// but props parameter is still available</span>
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(props); <span class="hljs-comment">// prints { name: 'John', age: 42 }</span>
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-comment">// no difference outside constructor</span>
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>); <span class="hljs-comment">// prints { name: 'John', age: 42 }</span>
    }
}
</code></pre>
<!-- codeblock-end -->

The above code snippets reveals that `this.props` is different only within the constructor. It would be the same outside the constructor.

========== Id ==========  
284

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#284-What-is-the-purpose-of-using-super-constru

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
