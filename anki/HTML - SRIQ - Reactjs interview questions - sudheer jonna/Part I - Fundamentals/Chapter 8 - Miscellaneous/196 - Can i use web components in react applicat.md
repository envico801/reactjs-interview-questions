========== Question ==========  

### Can I use web components in react application?  

========== Answer ==========  

Yes, you can use web components in a react application. Even though many developers won't use this combination, it may require especially if you are using third-party UI components that are written using Web Components.

For example, let us use `Vaadin` date picker web component as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-string">'./App.css'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-string">'@vaadin/vaadin-date-picker'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'App'</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">vaadin-date-picker</span> <span class="hljs-attr">label</span>=<span class="hljs-string">'When were you born?'</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">vaadin-date-picker</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
196

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#196-Can-i-use-web-components-in-react-applicat

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
