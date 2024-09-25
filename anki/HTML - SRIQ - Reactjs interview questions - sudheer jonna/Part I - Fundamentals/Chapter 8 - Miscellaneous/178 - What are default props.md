========== Question ==========  

### What are default props?  

========== Answer ==========  

The _defaultProps_ can be defined as a property on the component to set the default values for the props. These default props are used when props not supplied(i.e., undefined props), but not for `null` or `0` as props. That means, If you provide null value then it remains null value. It's the same behavior with 0 as well.

For example, let us create color default prop for the button component,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title class_">MyButton</span> {
  <span class="hljs-comment">// ...</span>
}
<span class="hljs-title class_">MyButton</span>.<span class="hljs-property">defaultProps</span> = {
  <span class="hljs-attr">color</span>: <span class="hljs-string">"red"</span>,
};
</code></pre>
<!-- codeblock-end -->

If `props.color` is not provided then it will set the default value to 'red'. i.e, Whenever you try to access the color prop it uses the default value

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">MyButton</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyButton</span> /></span></span>; <span class="hljs-comment">// props.color will contain red value</span>
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
178

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#178-What-are-default-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
