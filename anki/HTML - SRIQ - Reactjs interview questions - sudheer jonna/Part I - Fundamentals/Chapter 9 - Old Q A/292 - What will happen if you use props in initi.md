========== Question ==========  

### What will happen if you use props in initial state?  

========== Answer ==========  

If the props on the component are changed without the component being refreshed, the new prop value will never be displayed because the constructor function will never update the current state of the component. The initialization of state from props only runs when the component is first created.

The below component won't display the updated input value:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">records</span>: [],
            <span class="hljs-attr">inputValue</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">inputValue</span>,
        };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{this.state.inputValue}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

Using props inside render method will update the value:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">record</span>: [],
        };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{this.props.inputValue}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
292

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#292-What-will-happen-if-you-use-props-in-initi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
