========== Question ==========  

### How to use class field declarations syntax in React classes?  

========== Answer ==========  

React Class Components can be made much more concise using the class field declarations. You can initialize the local state without using the constructor and declare class methods by using arrow functions without the extra need to bind them.

Let's take a counter example to demonstrate class field declarations for state without using constructor and methods without binding,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Counter</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    state = { <span class="hljs-attr">value</span>: <span class="hljs-number">0</span> };
    handleIncrement = <span class="hljs-function">() =></span> {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">prevState</span>) =></span> ({
            <span class="hljs-attr">value</span>: prevState.<span class="hljs-property">value</span> + <span class="hljs-number">1</span>,
        }));
    };
    handleDecrement = <span class="hljs-function">() =></span> {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">prevState</span>) =></span> ({
            <span class="hljs-attr">value</span>: prevState.<span class="hljs-property">value</span> - <span class="hljs-number">1</span>,
        }));
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                {this.state.value}
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleIncrement}</span>></span>+<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleDecrement}</span>></span>-<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
327

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#327-How-to-use-class-field-declarations-syntax

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
