========== Question ==========  

### Whats the purpose of `at` symbol in the Redux connect decorator?  

========== Answer ==========  

The **@** symbol is in fact a JavaScript expression used to signify decorators. _Decorators_ make it possible to annotate and modify classes and properties at design time.

Let's take an example setting up Redux without and with a decorator.

-   **Without decorator:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
        <span class="hljs-keyword">import</span> * <span class="hljs-keyword">as</span> actionCreators <span class="hljs-keyword">from</span> <span class="hljs-string">'./actionCreators'</span>;
        <span class="hljs-keyword">import</span> { bindActionCreators } <span class="hljs-keyword">from</span> <span class="hljs-string">'redux'</span>;
        <span class="hljs-keyword">import</span> { connect } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-redux'</span>;
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">mapStateToProps</span>(<span class="hljs-params">state</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">todos</span>: state.<span class="hljs-property">todos</span> };
        }
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">mapDispatchToProps</span>(<span class="hljs-params">dispatch</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">actions</span>: <span class="hljs-title function_">bindActionCreators</span>(actionCreators, dispatch) };
        }
        <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyApp</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-comment">// ...define your main app here</span>
        }
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">connect</span>(mapStateToProps, mapDispatchToProps)(<span class="hljs-title class_">MyApp</span>);
        </code></pre>
    <!-- codeblock-end -->

-   **With decorator:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
        <span class="hljs-keyword">import</span> * <span class="hljs-keyword">as</span> actionCreators <span class="hljs-keyword">from</span> <span class="hljs-string">'./actionCreators'</span>;
        <span class="hljs-keyword">import</span> { bindActionCreators } <span class="hljs-keyword">from</span> <span class="hljs-string">'redux'</span>;
        <span class="hljs-keyword">import</span> { connect } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-redux'</span>;
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">mapStateToProps</span>(<span class="hljs-params">state</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">todos</span>: state.<span class="hljs-property">todos</span> };
        }
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">mapDispatchToProps</span>(<span class="hljs-params">dispatch</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">actions</span>: <span class="hljs-title function_">bindActionCreators</span>(actionCreators, dispatch) };
        }
        @<span class="hljs-title function_">connect</span>(mapStateToProps, mapDispatchToProps)
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyApp</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-comment">// ...define your main app here</span>
        }
        </code></pre>
    <!-- codeblock-end -->

The above examples are almost similar except the usage of decorator. The decorator syntax isn't built into any JavaScript runtimes yet, and is still experimental and subject to change. You can use babel for the decorators support.

========== Id ==========  
322

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#322-Whats-the-purpose-of-at-symbol-in-the-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
