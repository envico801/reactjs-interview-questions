========== Question ==========  

### Does the statics object work with ES6 classes in React?  

========== Answer ==========  

No, `statics` only works with `React.createClass()`:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">someComponent = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createClass</span>({
    <span class="hljs-attr">statics</span>: {
        <span class="hljs-attr">someMethod</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
            <span class="hljs-comment">// ..</span>
        },
    },
});
</code></pre>
<!-- codeblock-end -->

But you can write statics inside ES6+ classes as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Component</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-keyword">static</span> propTypes = {
        <span class="hljs-comment">// ...</span>
    };
    <span class="hljs-keyword">static</span> <span class="hljs-title function_">someMethod</span>(<span class="hljs-params"></span>) {
        <span class="hljs-comment">// ...</span>
    }
}
</code></pre>
<!-- codeblock-end -->

or writing them outside class as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Component</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
   ....
}
<span class="hljs-title class_">Component</span>.<span class="hljs-property">propTypes</span> = {...}
<span class="hljs-title class_">Component</span>.<span class="hljs-property">someMethod</span> = <span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){....}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
324

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#324-Does-the-statics-object-work-with-es6-clas

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
