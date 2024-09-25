========== Question ==========  

### What is the difference between `mapStateToProps()` and `mapDispatchToProps()`?  

========== Answer ==========  

`mapStateToProps()` is a utility which helps your component get updated state (which is updated by some other components):

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">mapStateToProps</span> = (<span class="hljs-params">state</span>) => {
    <span class="hljs-keyword">return</span> {
        <span class="hljs-attr">todos</span>: <span class="hljs-title function_">getVisibleTodos</span>(state.<span class="hljs-property">todos</span>, state.<span class="hljs-property">visibilityFilter</span>),
    };
};
</code></pre>
<!-- codeblock-end -->

`mapDispatchToProps()` is a utility which will help your component to fire an action event (dispatching action which may cause change of application state):

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">mapDispatchToProps</span> = (<span class="hljs-params">dispatch</span>) => {
    <span class="hljs-keyword">return</span> {
        <span class="hljs-attr">onTodoClick</span>: <span class="hljs-function">(<span class="hljs-params">id</span>) =></span> {
            <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">toggleTodo</span>(id));
        },
    };
};
</code></pre>
<!-- codeblock-end -->

It is recommended to always use the “object shorthand” form for the `mapDispatchToProps`.

Redux wraps it in another function that looks like (…args) => dispatch(onTodoClick(…args)), and pass that wrapper function as a prop to your component.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> mapDispatchToProps = {
    onTodoClick,
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
106

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#106-What-is-the-difference-between-mapstateto

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
