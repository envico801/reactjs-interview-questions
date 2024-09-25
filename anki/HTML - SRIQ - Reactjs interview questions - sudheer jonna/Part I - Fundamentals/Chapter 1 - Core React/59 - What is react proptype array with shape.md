========== Question ==========  

### What is React proptype array with shape?  

========== Answer ==========  

If you want to pass an array of objects to a component with a particular shape then use `React.PropTypes.shape()` as an argument to `React.PropTypes.arrayOf()`.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title class_">ReactComponent</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">arrayWithShape</span>: <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-title function_">arrayOf</span>(
        <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-title function_">shape</span>({
            <span class="hljs-attr">color</span>: <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-property">string</span>.<span class="hljs-property">isRequired</span>,
            <span class="hljs-attr">fontSize</span>: <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-property">number</span>.<span class="hljs-property">isRequired</span>,
        }),
    ).<span class="hljs-property">isRequired</span>,
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
59

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#59-What-is-react-proptype-array-with-shape

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
