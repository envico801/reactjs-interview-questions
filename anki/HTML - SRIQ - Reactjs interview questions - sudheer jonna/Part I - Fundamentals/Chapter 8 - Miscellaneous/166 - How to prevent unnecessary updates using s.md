========== Question ==========  

### How to prevent unnecessary updates using setState?  

========== Answer ==========  

You can compare the current value of the state with an existing state value and decide whether to rerender the page or not. If the values are the same then you need to return **null** to stop re-rendering otherwise return the latest state value.

For example, the user profile information is conditionally rendered as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">getUserProfile = <span class="hljs-function">(<span class="hljs-params">user</span>) =></span> {
    <span class="hljs-keyword">const</span> latestAddress = user.<span class="hljs-property">address</span>;
    <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">state</span>) =></span> {
        <span class="hljs-keyword">if</span> (state.<span class="hljs-property">address</span> === latestAddress) {
            <span class="hljs-keyword">return</span> <span class="hljs-literal">null</span>;
        } <span class="hljs-keyword">else</span> {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">title</span>: latestAddress };
        }
    });
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
166

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#166-How-to-prevent-unnecessary-updates-using-s

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
