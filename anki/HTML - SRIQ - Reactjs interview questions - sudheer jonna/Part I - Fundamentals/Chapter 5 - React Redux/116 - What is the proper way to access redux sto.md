========== Question ==========  

### What is the proper way to access Redux store?  

========== Answer ==========  

The best way to access your store in a component is to use the `connect()` function, that creates a new component that wraps around your existing one. This pattern is called _Higher-Order Components_, and is generally the preferred way of extending a component's functionality in React. This allows you to map state and action creators to your component, and have them passed in automatically as your store updates.

Let's take an example of `<FilterLink>` component using connect:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { connect } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-redux'</span>;
<span class="hljs-keyword">import</span> { setVisibilityFilter } <span class="hljs-keyword">from</span> <span class="hljs-string">'../actions'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">Link</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'../components/Link'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">mapStateToProps</span> = (<span class="hljs-params">state, ownProps</span>) => ({
    <span class="hljs-attr">active</span>: ownProps.<span class="hljs-property">filter</span> === state.<span class="hljs-property">visibilityFilter</span>,
});
<span class="hljs-keyword">const</span> <span class="hljs-title function_">mapDispatchToProps</span> = (<span class="hljs-params">dispatch, ownProps</span>) => ({
    <span class="hljs-attr">onClick</span>: <span class="hljs-function">() =></span> <span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">setVisibilityFilter</span>(ownProps.<span class="hljs-property">filter</span>)),
});
<span class="hljs-keyword">const</span> <span class="hljs-title class_">FilterLink</span> = <span class="hljs-title function_">connect</span>(mapStateToProps, mapDispatchToProps)(<span class="hljs-title class_">Link</span>);
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">FilterLink</span>;
</code></pre>
<!-- codeblock-end -->

Due to it having quite a few performance optimizations and generally being less likely to cause bugs, the Redux developers almost always recommend using `connect()` over accessing the store directly (using context API).

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title class_">MyComponent</span> {
  <span class="hljs-title function_">someMethod</span>(<span class="hljs-params"></span>) {
    <span class="hljs-title function_">doSomethingWith</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>.<span class="hljs-property">store</span>);
  }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
116

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#116-What-is-the-proper-way-to-access-redux-sto

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
