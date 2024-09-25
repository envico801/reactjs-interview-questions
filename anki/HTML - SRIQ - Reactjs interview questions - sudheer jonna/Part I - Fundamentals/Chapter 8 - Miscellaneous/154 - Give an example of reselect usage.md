========== Question ==========  

### # Give an example of Reselect usage?  

========== Answer ==========  

Let's take calculations and different amounts of a shipment order with the simplified usage of Reselect:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { createSelector } <span class="hljs-keyword">from</span> <span class="hljs-string">'reselect'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">shopItemsSelector</span> = (<span class="hljs-params">state</span>) => state.<span class="hljs-property">shop</span>.<span class="hljs-property">items</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">taxPercentSelector</span> = (<span class="hljs-params">state</span>) => state.<span class="hljs-property">shop</span>.<span class="hljs-property">taxPercent</span>;
<span class="hljs-keyword">const</span> subtotalSelector = <span class="hljs-title function_">createSelector</span>(shopItemsSelector, <span class="hljs-function">(<span class="hljs-params">items</span>) =></span> items.<span class="hljs-title function_">reduce</span>(<span class="hljs-function">(<span class="hljs-params">acc, item</span>) =></span> acc + item.<span class="hljs-property">value</span>, <span class="hljs-number">0</span>));
<span class="hljs-keyword">const</span> taxSelector = <span class="hljs-title function_">createSelector</span>(subtotalSelector, taxPercentSelector, <span class="hljs-function">(<span class="hljs-params">subtotal, taxPercent</span>) =></span> subtotal * (taxPercent / <span class="hljs-number">100</span>));
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> totalSelector = <span class="hljs-title function_">createSelector</span>(subtotalSelector, taxSelector, <span class="hljs-function">(<span class="hljs-params">subtotal, tax</span>) =></span> ({ <span class="hljs-attr">total</span>: subtotal + tax }));
<span class="hljs-keyword">let</span> exampleState = {
    <span class="hljs-attr">shop</span>: {
        <span class="hljs-attr">taxPercent</span>: <span class="hljs-number">8</span>,
        <span class="hljs-attr">items</span>: [
            { <span class="hljs-attr">name</span>: <span class="hljs-string">'apple'</span>, <span class="hljs-attr">value</span>: <span class="hljs-number">1.2</span> },
            { <span class="hljs-attr">name</span>: <span class="hljs-string">'orange'</span>, <span class="hljs-attr">value</span>: <span class="hljs-number">0.95</span> },
        ],
    },
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">subtotalSelector</span>(exampleState)); <span class="hljs-comment">// 2.15</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">taxSelector</span>(exampleState)); <span class="hljs-comment">// 0.172</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">totalSelector</span>(exampleState)); <span class="hljs-comment">// { total: 2.322 }</span>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
154

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#154-Give-an-example-of-reselect-usage

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
