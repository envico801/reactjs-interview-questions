========== Question ==========  

### How do you update rendered elements?  

========== Answer ==========  

You can update UI(represented by rendered element) by passing the newly created element to ReactDOM's render method.

For example, lets take a ticking clock example, where it updates the time by calling render method multiple times,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">tick</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> element = (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Hello, world!<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>It is {new Date().toLocaleTimeString()}.<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
    <span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(element, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'root'</span>));
}
<span class="hljs-built_in">setInterval</span>(tick, <span class="hljs-number">1000</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
189

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#189-How-do-you-update-rendered-elements

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
