========== Question ==========  

### What is state mutation and how to prevent it?  

========== Answer ==========  

`State mutation` happens when you try to update the state of a component without actually using `setState` function. This can happen when you are trying to do some computations using a state variable and unknowingly save the result in the same state variable. This is the main reason why it is advised to return new instances of state variables from the reducers by using Object.assign({}, ...) or spread syntax.

This can cause unknown issues in the UI as the value of the state variable got updated without telling React to check what all components were being affected from this update and it can cause UI bugs.

Ex:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">A</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.component</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-variable language_">super</span>(props);
    <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
      <span class="hljs-attr">loading</span>: <span class="hljs-literal">false</span>
    }
 }
<span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">let</span> { loading } = <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>;
  loading = (<span class="hljs-function">() =></span> <span class="hljs-literal">true</span>)(); <span class="hljs-comment">// Trying to perform an operation and directly saving in a state variable</span>
}
</code></pre>
<!-- codeblock-end -->

**How to prevent it:** Make sure your state variables are immutable by either enforcing immutability by using plugins like Immutable.js, always using `setState` to make updates, and returning new instances in reducers when sending updated state values.

========== Id ==========  
359

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#359-What-is-state-mutation-and-how-to-prevent

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
