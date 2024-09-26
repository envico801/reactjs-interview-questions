========== Question ==========  

### Are custom DOM attributes supported in React v16?  

========== Answer ==========  

Yes. In the past, React used to ignore unknown DOM attributes. If you wrote JSX with an attribute that React doesn't recognize, React would just skip it.

For example, let's take a look at the below attribute:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;div mycustomattribute={<span class="hljs-string">'something'</span>} />
</code></pre>
<!-- codeblock-end -->

Would render an empty div to the DOM with React v15:

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> /></span>
</code></pre>
<!-- codeblock-end -->

In React v16 any unknown attributes will end up in the DOM:

<!-- codeblock-start -->
<pre><code class="hljs language-html"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">mycustomattribute</span>=<span class="hljs-string">"something"</span> /></span>
</code></pre>
<!-- codeblock-end -->

This is useful for supplying browser-specific non-standard attributes, trying new DOM APIs, and integrating with opinionated third-party libraries.

========== Id ==========  
56

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#56-Are-custom-dom-attributes-supported-in-rea

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store