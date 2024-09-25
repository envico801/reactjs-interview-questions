========== Question ==========  

### Why are inline ref callbacks or functions not recommended?  

========== Answer ==========  

If the ref callback is defined as an inline function, it will get called twice during updates, first with null and then again with the DOM element. This is because a new instance of the function is created with each render, so React needs to clear the old ref and set up the new one.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">UserForm</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    handleSubmit = <span class="hljs-function">() =></span> {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Input Value is: '</span>, <span class="hljs-variable language_">this</span>.<span class="hljs-property">input</span>.<span class="hljs-property">value</span>);
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">onSubmit</span>=<span class="hljs-string">{this.handleSubmit}</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'text'</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{(input)</span> =></span> (this.input = input)} /> // Access DOM input in handle submit
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'submit'</span>></span>Submit<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

But our expectation is for the ref callback to get called once, when the component mounts. One quick fix is to use the ES7 class property syntax to define the function

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">UserForm</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    handleSubmit = <span class="hljs-function">() =></span> {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'Input Value is: '</span>, <span class="hljs-variable language_">this</span>.<span class="hljs-property">input</span>.<span class="hljs-property">value</span>);
    };
    setSearchInput = <span class="hljs-function">(<span class="hljs-params">input</span>) =></span> {
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">input</span> = input;
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">onSubmit</span>=<span class="hljs-string">{this.handleSubmit}</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'text'</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.setSearchInput}</span> /></span> // Access DOM input in handle submit
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'submit'</span>></span>Submit<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
325

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#325-Why-are-inline-ref-callbacks-or-functions

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
