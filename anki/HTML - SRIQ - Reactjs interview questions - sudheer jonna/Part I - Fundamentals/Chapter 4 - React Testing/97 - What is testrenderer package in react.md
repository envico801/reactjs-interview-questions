========== Question ==========  

### What is `TestRenderer` package in React?  

========== Answer ==========  

This package provides a renderer that can be used to render components to pure JavaScript objects, without depending on the DOM or a native mobile environment. This package makes it easy to grab a snapshot of the platform view hierarchy (similar to a DOM tree) rendered by a ReactDOM or React Native without using a browser or `jsdom`.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">TestRenderer</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-test-renderer'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">Link</span> = (<span class="hljs-params">{ page, children }</span>) => <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">a</span> <span class="hljs-attr">href</span>=<span class="hljs-string">{page}</span>></span>{children}<span class="hljs-tag">&#x3C;/<span class="hljs-name">a</span>></span></span>;
<span class="hljs-keyword">const</span> testRenderer = <span class="hljs-title class_">TestRenderer</span>.<span class="hljs-title function_">create</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Link</span> <span class="hljs-attr">page</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">https:</span>//<span class="hljs-attr">www.facebook.com</span>/'}></span>{'Facebook'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">Link</span>></span></span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(testRenderer.<span class="hljs-title function_">toJSON</span>());
<span class="hljs-comment">// {</span>
<span class="hljs-comment">//   type: 'a',</span>
<span class="hljs-comment">//   props: { href: 'https://www.facebook.com/' },</span>
<span class="hljs-comment">//   children: [ 'Facebook' ]</span>
<span class="hljs-comment">// }</span>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
97

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 4 - React Testing

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-4-React-Testing::#97-What-is-testrenderer-package-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
