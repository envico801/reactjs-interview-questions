========== Question ==========  

### What are Keyed Fragments?  

========== Answer ==========  

The Fragments declared with the explicit <React.Fragment> syntax may have keys. The general use case is mapping a collection to an array of fragments as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Glossary</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">dl</span>></span>
            {props.items.map((item) => (
                // Without the `key`, React will fire a key warning
                <span class="hljs-tag">&#x3C;<span class="hljs-name">React.Fragment</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{item.id}</span>></span>
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">dt</span>></span>{item.term}<span class="hljs-tag">&#x3C;/<span class="hljs-name">dt</span>></span>
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">dd</span>></span>{item.description}<span class="hljs-tag">&#x3C;/<span class="hljs-name">dd</span>></span>
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">React.Fragment</span>></span>
            ))}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">dl</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

**Note:** key is the only attribute that can be passed to Fragment. In the future, there might be a support for additional attributes, such as event handlers.

========== Id ==========  
182

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#182-What-are-keyed-fragments

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
