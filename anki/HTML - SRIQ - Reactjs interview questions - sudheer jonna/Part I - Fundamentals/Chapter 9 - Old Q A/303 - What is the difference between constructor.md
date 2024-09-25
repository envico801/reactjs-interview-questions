========== Question ==========  

### What is the difference between constructor and getInitialState?  

========== Answer ==========  

You should initialize state in the constructor when using ES6 classes, and `getInitialState()` method when using `React.createClass()`.

**Using ES6 classes:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-comment">/* initial state */</span>
        };
    }
}
</code></pre>
<!-- codeblock-end -->

**Using `React.createClass()`:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">MyComponent</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createClass</span>({
    <span class="hljs-title function_">getInitialState</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> {
            <span class="hljs-comment">/* initial state */</span>
        };
    },
});
</code></pre>
<!-- codeblock-end -->

**Note:** `React.createClass()` is deprecated and removed in React v16. Use plain JavaScript classes instead.

========== Id ==========  
303

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#303-What-is-the-difference-between-constructor

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
