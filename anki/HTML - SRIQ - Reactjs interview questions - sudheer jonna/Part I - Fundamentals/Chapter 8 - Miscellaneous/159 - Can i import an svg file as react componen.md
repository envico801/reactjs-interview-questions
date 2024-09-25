========== Question ==========  

### Can I import an SVG file as react component?  

========== Answer ==========  

You can import SVG directly as component instead of loading it as a file. This feature is available with `react-scripts@2.0.0` and higher.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">ReactComponent</span> <span class="hljs-keyword">as</span> <span class="hljs-title class_">Logo</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./logo.svg'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">App</span> = (<span class="hljs-params"></span>) => (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
        {/* Logo is an actual react component */}
        <span class="hljs-tag">&#x3C;<span class="hljs-name">Logo</span> /></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
);
</code></pre>
<!-- codeblock-end -->

**Note**: Don't forget about the curly braces in the import.

========== Id ==========  
159

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#159-Can-i-import-an-svg-file-as-react-componen

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
