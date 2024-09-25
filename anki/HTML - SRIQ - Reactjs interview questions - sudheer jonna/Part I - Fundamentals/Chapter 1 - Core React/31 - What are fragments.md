========== Question ==========  

### What are fragments?  

========== Answer ==========  

It's a common pattern or practice in React for a component to return multiple elements. _Fragments_ let you group a list of children without adding extra nodes to the DOM.

You need to use either `<Fragment>` or a shorter syntax having empty tag (`<></>`).

Below is the example of how to use fragment inside _Story_ component.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Story</span>(<span class="hljs-params">{ title, description, date }</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Fragment</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{description}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{date}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">Fragment</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

It is also possible to render list of fragments inside a loop with the mandatory **key** attribute supplied.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">StoryBook</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> stories.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">story</span>) =></span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Fragment</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{story.id}</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{story.title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{story.description}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{story.date}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">Fragment</span>></span></span>
    ));
}
</code></pre>
<!-- codeblock-end -->

Usually, you don't need to use `<Fragment>` until there is a need of _key_ attribute. The usage of shorter syntax looks like below.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Story</span>(<span class="hljs-params">{ title, description, date }</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{description}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{date}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
31

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#31-What-are-fragments

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
