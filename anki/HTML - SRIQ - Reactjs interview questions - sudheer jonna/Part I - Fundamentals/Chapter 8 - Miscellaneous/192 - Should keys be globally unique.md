========== Question ==========  

### Should keys be globally unique?  

========== Answer ==========  

The keys used within arrays should be unique among their siblings but they don’t need to be globally unique. i.e, You can use the same keys with two different arrays.

For example, the below `Book` component uses two arrays with different arrays,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Book</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">const</span> index = (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
            {props.pages.map((page) => (
                <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{page.id}</span>></span>{page.title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
            ))}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
    );
    <span class="hljs-keyword">const</span> content = props.<span class="hljs-property">pages</span>.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">page</span>) =></span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{page.id}</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h3</span>></span>{page.title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h3</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{page.content}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{page.pageNumber}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    ));
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            {index}
            <span class="hljs-tag">&#x3C;<span class="hljs-name">hr</span> /></span>
            {content}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
192

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#192-Should-keys-be-globally-unique

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
