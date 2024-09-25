========== Question ==========  

### How to perform automatic redirect after login?  

========== Answer ==========  

The `react-router` package provides `<Redirect>` component in React Router. Rendering a `<Redirect>` will navigate to a new location. Like server-side redirects, the new location will override the current location in the history stack.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> { <span class="hljs-title class_">Redirect</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">"react-router"</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title class_">Login</span> {
    <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">isLoggedIn</span> === <span class="hljs-literal">true</span>) {
      <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Redirect</span> <span class="hljs-attr">to</span>=<span class="hljs-string">"/your/redirect/page"</span> /></span></span>;
    } <span class="hljs-keyword">else</span> {
      <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{"Login Please"}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

  <details><summary><b>See Class</b></summary>

  <p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { <span class="hljs-title class_">Component</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> { <span class="hljs-title class_">Redirect</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">LoginComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">isLoggedIn</span> === <span class="hljs-literal">true</span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Redirect</span> <span class="hljs-attr">to</span>=<span class="hljs-string">'/your/redirect/page'</span> /></span></span>;
        } <span class="hljs-keyword">else</span> {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{'Login Please'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
        }
    }
}
</code></pre>
<!-- codeblock-end -->

   </p>

   </details>

========== Id ==========  
89

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#89-How-to-perform-automatic-redirect-after-lo

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
