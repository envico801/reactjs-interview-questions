========== Question ==========  

### How to combine multiple inline style objects?  

========== Answer ==========  

You can use _spread operator_ in regular React:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button style={{ ...styles.<span class="hljs-property">panel</span>.<span class="hljs-property">button</span>, ...styles.<span class="hljs-property">panel</span>.<span class="hljs-property">submitButton</span> }}>{<span class="hljs-string">'Submit'</span>}&#x3C;/button>
</code></pre>
<!-- codeblock-end -->

If you're using React Native then you can use the array notation:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;button style={[styles.<span class="hljs-property">panel</span>.<span class="hljs-property">button</span>, styles.<span class="hljs-property">panel</span>.<span class="hljs-property">submitButton</span>]}>{<span class="hljs-string">'Submit'</span>}&#x3C;/button>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
64

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#64-How-to-combine-multiple-inline-style-objec

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
