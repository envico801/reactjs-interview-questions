========== Question ==========  

### What is ReactDOMServer?  

========== Answer ==========  

The `ReactDOMServer` object enables you to render components to static markup (typically used on node server). This object is mainly used for _server-side rendering_ (SSR). The following methods can be used in both the server and browser environments:

1. `renderToString()`

2. `renderToStaticMarkup()`

For example, you generally run a Node-based web server like Express, Hapi, or Koa, and you call `renderToString` to render your root component to a string, which you then send as response.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// using Express</span>
<span class="hljs-keyword">import</span> { renderToString } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom/server'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">MyPage</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./MyPage'</span>;
app.<span class="hljs-title function_">get</span>(<span class="hljs-string">'/'</span>, <span class="hljs-function">(<span class="hljs-params">req, res</span>) =></span> {
    res.<span class="hljs-title function_">write</span>(<span class="hljs-string">'&#x3C;!DOCTYPE html>&#x3C;html>&#x3C;head>&#x3C;title>My Page&#x3C;/title>&#x3C;/head>&#x3C;body>'</span>);
    res.<span class="hljs-title function_">write</span>(<span class="hljs-string">'&#x3C;div id="content">'</span>);
    res.<span class="hljs-title function_">write</span>(<span class="hljs-title function_">renderToString</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">MyPage</span> /></span></span>));
    res.<span class="hljs-title function_">write</span>(<span class="hljs-string">'&#x3C;/div>&#x3C;/body>&#x3C;/html>'</span>);
    res.<span class="hljs-title function_">end</span>();
});
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
41

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#41-What-is-reactdomserver

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
