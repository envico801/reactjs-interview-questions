========== Question ==========  

### Is it possible to use react without JSX?  

========== Answer ==========  

Yes, JSX is not mandatory for using React. Actually it is convenient when you don’t want to set up compilation in your build environment. Each JSX element is just syntactic sugar for calling `React.createElement(component, props, ...children)`.

For example, let us take a greeting example with JSX,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Greeting</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>Hello {this.props.message}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    }
}
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Greeting</span> <span class="hljs-attr">message</span>=<span class="hljs-string">'World'</span> /></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'root'</span>));
</code></pre>
<!-- codeblock-end -->

You can write the same code without JSX as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Greeting</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-string">'div'</span>, <span class="hljs-literal">null</span>, <span class="hljs-string">`Hello <span class="hljs-subst">${<span class="hljs-variable language_">this</span>.props.message}</span>`</span>);
    }
}
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="hljs-title class_">React</span>.<span class="hljs-title function_">createElement</span>(<span class="hljs-title class_">Greeting</span>, { <span class="hljs-attr">message</span>: <span class="hljs-string">'World'</span> }, <span class="hljs-literal">null</span>), <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'root'</span>));
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
353

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#353-Is-it-possible-to-use-react-without-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
