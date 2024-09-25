========== Question ==========  

### How to use `connect()` from React Redux?  

========== Answer ==========  

You need to follow two steps to use your store in your container:

1.  **Use `mapStateToProps()`:** It maps the state variables from your store to the props that you specify.

2.  **Connect the above props to your container:** The object returned by the `mapStateToProps` function is connected to the container. You can import `connect()` from `react-redux`.

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
        <span class="hljs-keyword">import</span> { connect } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-redux'</span>;
        <span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{this.props.containerData}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
            }
        }
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">mapStateToProps</span>(<span class="hljs-params">state</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">containerData</span>: state.<span class="hljs-property">data</span> };
        }
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">connect</span>(mapStateToProps)(<span class="hljs-title class_">App</span>);
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
321

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#321-How-to-use-connect-from-react-redux

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
