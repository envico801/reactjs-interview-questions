========== Question ==========  

### How to get history on React Router v4?  

========== Answer ==========  

Below are the list of steps to get history object on React Router v4,

1.  Create a module that exports a `history` object and import this module across the project.

    For example, create `history.js` file:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> { createBrowserHistory } <span class="hljs-keyword">from</span> <span class="hljs-string">'history'</span>;
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">createBrowserHistory</span>({
            <span class="hljs-comment">/* pass a configuration object here if needed */</span>
        });
        </code></pre>
    <!-- codeblock-end -->

2.  You should use the `<Router>` component instead of built-in routers. Import the above `history.js` inside `index.js` file:

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">import</span> { <span class="hljs-title class_">Router</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router-dom'</span>;
        <span class="hljs-keyword">import</span> history <span class="hljs-keyword">from</span> <span class="hljs-string">'./history'</span>;
        <span class="hljs-keyword">import</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./App'</span>;
        <span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Router</span> <span class="hljs-attr">history</span>=<span class="hljs-string">{history}</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">Router</span>></span></span>,
            holder,
        );
        </code></pre>
    <!-- codeblock-end -->

3.  You can also use push method of `history` object similar to built-in history object:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-comment">// some-other-file.js</span>
        <span class="hljs-keyword">import</span> history <span class="hljs-keyword">from</span> <span class="hljs-string">'./history'</span>;
        history.<span class="hljs-title function_">push</span>(<span class="hljs-string">'/go-here'</span>);
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
88

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#88-How-to-get-history-on-react-router-v4

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
