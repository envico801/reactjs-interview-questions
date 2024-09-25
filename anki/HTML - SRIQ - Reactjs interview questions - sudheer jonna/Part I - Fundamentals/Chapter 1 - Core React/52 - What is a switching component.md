========== Question ==========  

### What is a switching component?  

========== Answer ==========  

A _switching component_ is a component that renders one of many components. We need to use object to map prop values to components.

For example, a switching component to display different pages based on `page` prop:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">HomePage</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./HomePage'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">AboutPage</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./AboutPage'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ServicesPage</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./ServicesPage'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ContactPage</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./ContactPage'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-variable constant_">PAGES</span> = {
    <span class="hljs-attr">home</span>: <span class="hljs-title class_">HomePage</span>,
    <span class="hljs-attr">about</span>: <span class="hljs-title class_">AboutPage</span>,
    <span class="hljs-attr">services</span>: <span class="hljs-title class_">ServicesPage</span>,
    <span class="hljs-attr">contact</span>: <span class="hljs-title class_">ContactPage</span>,
};
<span class="hljs-keyword">const</span> <span class="hljs-title function_">Page</span> = (<span class="hljs-params">props</span>) => {
    <span class="hljs-keyword">const</span> <span class="hljs-title class_">Handler</span> = <span class="hljs-variable constant_">PAGES</span>[props.<span class="hljs-property">page</span>] || <span class="hljs-title class_">ContactPage</span>;
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Handler</span> {<span class="hljs-attr">...props</span>} /></span></span>;
};
<span class="hljs-comment">// The keys of the PAGES object can be used in the prop types to catch dev-time errors.</span>
<span class="hljs-title class_">Page</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">page</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-title function_">oneOf</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">keys</span>(<span class="hljs-variable constant_">PAGES</span>)).<span class="hljs-property">isRequired</span>,
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
52

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#52-What-is-a-switching-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
