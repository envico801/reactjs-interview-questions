========== Question ==========  

### Give an example on How to use context?  

========== Answer ==========  

**Context** is designed to share data that can be considered **global** for a tree of React components.

For example, in the code below lets manually thread through a “theme” prop in order to style the Button component.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//Lets create a context with a default theme value "luna"</span>
<span class="hljs-keyword">const</span> <span class="hljs-title class_">ThemeContext</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createContext</span>(<span class="hljs-string">'luna'</span>);
<span class="hljs-comment">// Create App component where it uses provider to pass theme value in the tree</span>
<span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ThemeContext.Provider</span> <span class="hljs-attr">value</span>=<span class="hljs-string">'nova'</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Toolbar</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">ThemeContext.Provider</span>></span></span>
        );
    }
}
<span class="hljs-comment">// A middle component where you don't need to pass theme prop anymore</span>
<span class="hljs-keyword">function</span> <span class="hljs-title function_">Toolbar</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">ThemedButton</span> /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
<span class="hljs-comment">// Lets read theme value in the button component to use</span>
<span class="hljs-keyword">class</span> <span class="hljs-title class_">ThemedButton</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-keyword">static</span> contextType = <span class="hljs-title class_">ThemeContext</span>;
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Button</span> <span class="hljs-attr">theme</span>=<span class="hljs-string">{this.context}</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
345

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#345-Give-an-example-on-how-to-use-context

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
