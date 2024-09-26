========== Question ==========  

### Must prop be named as render for render props?  

========== Answer ==========  

Even though the pattern named render props, you don’t have to use a prop named render to use this pattern. i.e, Any prop that is a function that a component uses to know what to render is technically a “render prop”. Lets take an example with the children prop for render props,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">Mouse</span>
    children={<span class="hljs-function">(<span class="hljs-params">mouse</span>) =></span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>
            The mouse position is {mouse.x}, {mouse.y}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span></span>
    )}
/>
</code></pre>
<!-- codeblock-end -->

Actually children prop doesn’t need to be named in the list of “attributes” in JSX element. Instead, you can keep it directly inside element,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">Mouse</span>>
    {<span class="hljs-function">(<span class="hljs-params">mouse</span>) =></span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>
            The mouse position is {mouse.x}, {mouse.y}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span></span>
    )}
&#x3C;/<span class="hljs-title class_">Mouse</span>>
</code></pre>
<!-- codeblock-end -->

While using this above technique(without any name), explicitly state that children should be a function in your propTypes.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">Mouse</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">children</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">func</span>.<span class="hljs-property">isRequired</span>,
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
205

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#205-Must-prop-be-named-as-render-for-render-pr

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store