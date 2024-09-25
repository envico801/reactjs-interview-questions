========== Question ==========  

### How to re-render the view when the browser is resized?  

========== Answer ==========  

You can use the `useState` hook to manage the width and height state variables, and the `useEffect` hook to add and remove the `resize` event listener. The `[]` dependency array passed to useEffect ensures that the effect only runs once (on mount) and not on every re-render.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { useState, useEffect } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">WindowDimensions</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [dimensions, setDimensions] = <span class="hljs-title function_">useState</span>({
        <span class="hljs-attr">width</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerWidth</span>,
        <span class="hljs-attr">height</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerHeight</span>,
    });
    <span class="hljs-title function_">useEffect</span>(<span class="hljs-function">() =></span> {
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleResize</span>(<span class="hljs-params"></span>) {
            <span class="hljs-title function_">setDimensions</span>({
                <span class="hljs-attr">width</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerWidth</span>,
                <span class="hljs-attr">height</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerHeight</span>,
            });
        }
        <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'resize'</span>, handleResize);
        <span class="hljs-keyword">return</span> <span class="hljs-function">() =></span> <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">removeEventListener</span>(<span class="hljs-string">'resize'</span>, handleResize);
    }, []);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>
            {dimensions.width} x {dimensions.height}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

<details>

<summary><h4>Using Class Component</h4></summary>

You can listen to the `resize` event in `componentDidMount()` and then update the dimensions (`width` and `height`). You should remove the listener in `componentWillUnmount()` method.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">WindowDimensions</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">updateDimensions</span> = <span class="hljs-variable language_">this</span>.<span class="hljs-property">updateDimensions</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
    }
    <span class="hljs-title function_">componentWillMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">updateDimensions</span>();
    }
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">addEventListener</span>(<span class="hljs-string">'resize'</span>, <span class="hljs-variable language_">this</span>.<span class="hljs-property">updateDimensions</span>);
    }
    <span class="hljs-title function_">componentWillUnmount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">window</span>.<span class="hljs-title function_">removeEventListener</span>(<span class="hljs-string">'resize'</span>, <span class="hljs-variable language_">this</span>.<span class="hljs-property">updateDimensions</span>);
    }
    <span class="hljs-title function_">updateDimensions</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
            <span class="hljs-attr">width</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerWidth</span>,
            <span class="hljs-attr">height</span>: <span class="hljs-variable language_">window</span>.<span class="hljs-property">innerHeight</span>,
        });
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">span</span>></span>
                {this.state.width} x {this.state.height}
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">span</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

</details>

========== Id ==========  
65

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#65-How-to-re-render-the-view-when-the-browser

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
