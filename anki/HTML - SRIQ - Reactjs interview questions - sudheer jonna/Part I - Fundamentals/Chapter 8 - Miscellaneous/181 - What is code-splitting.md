========== Question ==========  

### What is code-splitting?  

========== Answer ==========  

Code-Splitting is a feature supported by bundlers like Webpack and Browserify which can create multiple bundles that can be dynamically loaded at runtime. The react project supports code splitting via dynamic import() feature.

For example, in the below code snippets, it will make moduleA.js and all its unique dependencies as a separate chunk that only loads after the user clicks the 'Load' button.

**moduleA.js**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> moduleA = <span class="hljs-string">'Hello'</span>;
<span class="hljs-keyword">export</span> { moduleA };
</code></pre>
<!-- codeblock-end -->

**App.js**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title class_">App</span> {
  <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleClick</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">import</span>(<span class="hljs-string">"./moduleA"</span>)
      .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">{ moduleA }</span>) =></span> {
        <span class="hljs-comment">// Use moduleA</span>
      })
      .<span class="hljs-title function_">catch</span>(<span class="hljs-function">(<span class="hljs-params">err</span>) =></span> {
        <span class="hljs-comment">// Handle failure</span>
      });
  };
 <span class="hljs-keyword">return</span> (
   <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
     <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick}</span>></span>Load<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
   <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
 );
}
</code></pre>
<!-- codeblock-end -->

  <details><summary><b>See Class</b></summary>

<p>

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { <span class="hljs-title class_">Component</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    handleClick = <span class="hljs-function">() =></span> {
        <span class="hljs-keyword">import</span>(<span class="hljs-string">'./moduleA'</span>)
            .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">{ moduleA }</span>) =></span> {
                <span class="hljs-comment">// Use moduleA</span>
            })
            .<span class="hljs-title function_">catch</span>(<span class="hljs-function">(<span class="hljs-params">err</span>) =></span> {
                <span class="hljs-comment">// Handle failure</span>
            });
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.handleClick}</span>></span>Load<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">App</span>;
</code></pre>
<!-- codeblock-end -->

  </p>

</details>

========== Id ==========  
181

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#181-What-is-code-splitting

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
