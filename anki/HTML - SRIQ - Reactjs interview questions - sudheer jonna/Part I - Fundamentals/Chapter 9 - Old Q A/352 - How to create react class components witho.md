========== Question ==========  

### How to create react class components without ES6?  

========== Answer ==========  

If you don’t use ES6 then you may need to use the create-react-class module instead. For default props, you need to define getDefaultProps() as a function on the passed object. Whereas for initial state, you have to provide a separate getInitialState method that returns the initial state.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> <span class="hljs-title class_">Greeting</span> = <span class="hljs-title function_">createReactClass</span>({
    <span class="hljs-attr">getDefaultProps</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> {
            <span class="hljs-attr">name</span>: <span class="hljs-string">'Jhohn'</span>,
        };
    },
    <span class="hljs-attr">getInitialState</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> { <span class="hljs-attr">message</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">message</span> };
    },
    <span class="hljs-attr">handleClick</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">message</span>);
    },
    <span class="hljs-attr">render</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Hello, {this.props.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
    },
});
</code></pre>
<!-- codeblock-end -->

**Note:** If you use createReactClass then auto binding is available for all methods. i.e, You don't need to use `.bind(this)` with in constructor for event handlers.

========== Id ==========  
352

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#352-How-to-create-react-class-components-witho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
