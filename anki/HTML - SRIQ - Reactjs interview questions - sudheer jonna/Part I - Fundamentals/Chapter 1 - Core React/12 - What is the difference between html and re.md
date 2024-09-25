========== Question ==========  

### What is the difference between HTML and React event handling?  

========== Answer ==========  

Below are some of the main differences between HTML and React event handling,

1. In HTML, the event name usually represents in _lowercase_ as a convention:

    <!-- codeblock-start -->
    <pre><code class="hljs language-html">
        <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">"activateLasers()"</span>></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        </code></pre>
    <!-- codeblock-end -->

    Whereas in React it follows _camelCase_ convention:

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">        &#x3C;button onClick={activateLasers}>
        </code></pre>
    <!-- codeblock-end -->

2. In HTML, you can return `false` to prevent default behavior:

    <!-- codeblock-start -->
    <pre><code class="hljs language-html">
        <span class="hljs-tag">&#x3C;<span class="hljs-name">a</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"#"</span> <span class="hljs-attr">onclick</span>=<span class="hljs-string">'console.log("The link was clicked."); return false;'</span> /></span>
        </code></pre>
    <!-- codeblock-end -->

    Whereas in React you must call `preventDefault()` explicitly:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleClick</span>(<span class="hljs-params">event</span>) {
            event.<span class="hljs-title function_">preventDefault</span>();
            <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'The link was clicked.'</span>);
        }
        </code></pre>
    <!-- codeblock-end -->

3. In HTML, you need to invoke the function by appending `()`

    Whereas in react you should not append `()` with the function name. (refer "activateLasers" function in the first point for example)

========== Id ==========  
12

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#12-What-is-the-difference-between-html-and-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
