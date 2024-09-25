========== Question ==========  

### How do you render Array, Strings and Numbers in React 16 Version?  

========== Answer ==========  

**Arrays**: Unlike older releases, you don't need to make sure **render** method return a single element in React16. You are able to return multiple sibling elements without a wrapping element by returning an array.

For example, let us take the below list of developers,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">ReactJSDevs</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">return</span> [<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">'1'</span>></span>John<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>, <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">'2'</span>></span>Jackie<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>, <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">'3'</span>></span>Jordan<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>];
};
</code></pre>
<!-- codeblock-end -->

You can also merge this array of items in another array component.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">JSDevs</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>Brad<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>Brodge<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">ReactJSDevs</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>Brandon<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
    );
};
</code></pre>
<!-- codeblock-end -->

**Strings and Numbers:** You can also return string and number type from the render method.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
 <span class="hljs-keyword">return</span> <span class="hljs-string">'Welcome to ReactJS questions'</span>;
}
<span class="hljs-comment">// Number</span>
<span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
 <span class="hljs-keyword">return</span> <span class="hljs-number">2018</span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
167

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#167-How-do-you-render-array-strings-and-numbe

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
