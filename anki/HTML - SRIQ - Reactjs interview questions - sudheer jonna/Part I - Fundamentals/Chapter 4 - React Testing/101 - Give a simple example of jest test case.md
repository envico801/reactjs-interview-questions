========== Question ==========  

### Give a simple example of Jest test case  

========== Answer ==========  

Let's write a test for a function that adds two numbers in `sum.js` file:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">sum</span> = (<span class="hljs-params">a, b</span>) => a + b;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> sum;
</code></pre>
<!-- codeblock-end -->

Create a file named `sum.test.js` which contains actual test:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> sum <span class="hljs-keyword">from</span> <span class="hljs-string">'./sum'</span>;
<span class="hljs-title function_">test</span>(<span class="hljs-string">'adds 1 + 2 to equal 3'</span>, <span class="hljs-function">() =></span> {
    <span class="hljs-title function_">expect</span>(<span class="hljs-title function_">sum</span>(<span class="hljs-number">1</span>, <span class="hljs-number">2</span>)).<span class="hljs-title function_">toBe</span>(<span class="hljs-number">3</span>);
});
</code></pre>
<!-- codeblock-end -->

And then add the following section to your `package.json`:

<!-- codeblock-start -->
<pre><code class="hljs language-json"><span class="hljs-punctuation">{</span>
    <span class="hljs-attr">"scripts"</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
        <span class="hljs-attr">"test"</span><span class="hljs-punctuation">:</span> <span class="hljs-string">"jest"</span>
    <span class="hljs-punctuation">}</span>
<span class="hljs-punctuation">}</span>
</code></pre>
<!-- codeblock-end -->

Finally, run `yarn test` or `npm test` and Jest will print a result:

<!-- codeblock-start -->
<pre><code class="hljs language-console"><span class="hljs-meta prompt_">
$ </span><span class="bash">yarn <span class="hljs-built_in">test</span></span>
PASS ./sum.test.js
✓ adds 1 + 2 to equal 3 (2ms)
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
101

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 4 - React Testing

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-4-React-Testing::#101-Give-a-simple-example-of-jest-test-case

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
