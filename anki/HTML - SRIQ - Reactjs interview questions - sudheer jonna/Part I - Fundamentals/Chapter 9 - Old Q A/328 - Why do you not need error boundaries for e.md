========== Question ==========  

### Why do you not need error boundaries for event handlers?  

========== Answer ==========  

Error boundaries do not catch errors inside event handlers.

React doesn’t need error boundaries to recover from errors in event handlers. Unlike the render method and lifecycle methods, the event handlers don’t happen during rendering. So if they throw, React still knows what to display on the screen.

If you need to catch an error inside an event handler, use the regular JavaScript try / catch statement:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">error</span>: <span class="hljs-literal">null</span> };
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span> = <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleClick</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
    }
    <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">try</span> {
            <span class="hljs-comment">// Do something that could throw</span>
        } <span class="hljs-keyword">catch</span> (error) {
            <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ error });
        }
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">if</span> (<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">error</span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Caught an error.<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
        }
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick}</span>></span>Click Me<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

Note that the above example is demonstrating regular JavaScript behavior and doesn’t use error boundaries.

========== Id ==========  
328

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#328-Why-do-you-not-need-error-boundaries-for-e

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
