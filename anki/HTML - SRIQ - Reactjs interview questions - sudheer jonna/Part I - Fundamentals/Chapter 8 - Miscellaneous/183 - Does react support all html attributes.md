========== Question ==========  

### Does React support all HTML attributes?  

========== Answer ==========  

As of React 16, both standard or custom DOM attributes are fully supported. Since React components often take both custom and DOM-related props, React uses the camelCase convention just like the DOM APIs.

Let us take few props with respect to standard HTML attributes,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;div tabIndex=<span class="hljs-string">"-1"</span> />      <span class="hljs-comment">// Just like node.tabIndex DOM API</span>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">"Button"</span> /></span></span> <span class="hljs-comment">// Just like node.className DOM API</span>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">readOnly</span>=<span class="hljs-string">{true}</span> /></span></span>  <span class="hljs-comment">// Just like node.readOnly DOM API</span>
</code></pre>
<!-- codeblock-end -->

These props work similarly to the corresponding HTML attributes, with the exception of the special cases. It also support all SVG attributes.

========== Id ==========  
183

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#183-Does-react-support-all-html-attributes

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
