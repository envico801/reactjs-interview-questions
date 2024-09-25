========== Question ==========  

### Why are String Refs legacy?  

========== Answer ==========  

If you worked with React before, you might be familiar with an older API where the `ref` attribute is a string, like `ref={'textInput'}`, and the DOM node is accessed as `this.refs.textInput`. We advise against it because _string refs have below issues_, and are considered legacy. String refs were **removed in React v16**.

1. They _force React to keep track of currently executing component_. This is problematic because it makes react module stateful, and thus causes weird errors when react module is duplicated in the bundle.

2. They are _not composable_ — if a library puts a ref on the passed child, the user can't put another ref on it. Callback refs are perfectly composable.

3. They _don't work with static analysis_ like Flow. Flow can't guess the magic that framework does to make the string ref appear on `this.refs`, as well as its type (which could be different). Callback refs are friendlier to static analysis.

4. It doesn't work as most people would expect with the "render callback" pattern (e.g. <DataGrid renderRow={this.renderRow} />)

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    renderRow = <span class="hljs-function">(<span class="hljs-params">index</span>) =></span> {
        <span class="hljs-comment">// This won't work. Ref will get attached to DataTable rather than MyComponent:</span>
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">input-</span>' + <span class="hljs-attr">index</span>} /></span></span>;
        <span class="hljs-comment">// This would work though! Callback refs are awesome.</span>
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{(input)</span> =></span> (this['input-' + index] = input)} /></span>;
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">DataTable</span> <span class="hljs-attr">data</span>=<span class="hljs-string">{this.props.data}</span> <span class="hljs-attr">renderRow</span>=<span class="hljs-string">{this.renderRow}</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
279

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#279-Why-are-string-refs-legacy

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
