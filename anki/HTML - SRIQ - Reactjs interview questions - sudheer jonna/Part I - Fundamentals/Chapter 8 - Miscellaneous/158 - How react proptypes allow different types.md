========== Question ==========  

### How React PropTypes allow different types for one prop?  

========== Answer ==========  

You can use `oneOfType()` method of `PropTypes`.

For example, the height property can be defined with either `string` or `number` type as below:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Component</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">size</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-title function_">oneOfType</span>([<span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">string</span>, <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">number</span>]),
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
158

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#158-How-react-proptypes-allow-different-types

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
