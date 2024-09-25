========== Question ==========  

### Should I learn ES6 before learning ReactJS?  

========== Answer ==========  

No, you don’t have to learn es2015/es6 to learn react. But you may find many resources or React ecosystem uses ES6 extensively. Let's see some of the frequently used ES6 features,

1.  **Destructuring:** To get props and use them in a component

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-comment">// in es 5</span>
        <span class="hljs-keyword">var</span> someData = <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">someData</span>;
        <span class="hljs-keyword">var</span> dispatch = <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">dispatch</span>;
        <span class="hljs-comment">// in es6</span>
        <span class="hljs-keyword">const</span> { someData, dispatch } = <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>;
        </code></pre>
    <!-- codeblock-end -->

2.  **Spread operator:** Helps in passing props down into a component

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-comment">// in es 5</span>
        &#x3C;<span class="hljs-title class_">SomeComponent</span> someData={<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">someData</span>} dispatch={<span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">dispatch</span>} />
        <span class="hljs-comment">// in es6</span>
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">SomeComponent</span> {<span class="hljs-attr">...this.props</span>} /></span></span>
        </code></pre>
    <!-- codeblock-end -->

3.  **Arrow functions:** Makes compact syntax

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-comment">// es 5</span>
        <span class="hljs-keyword">var</span> users = usersList.<span class="hljs-title function_">map</span>(<span class="hljs-keyword">function</span> (<span class="hljs-params">user</span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>{user.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>;
        });
        <span class="hljs-comment">// es 6</span>
        <span class="hljs-keyword">const</span> users = usersList.<span class="hljs-title function_">map</span>(<span class="hljs-function">(<span class="hljs-params">user</span>) =></span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>{user.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>);
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
229

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#229-Should-i-learn-es6-before-learning-reactjs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
