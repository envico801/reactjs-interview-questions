========== Question ==========  

### How to create refs?  

========== Answer ==========  

There are two approaches

1. This is a recently added approach. _Refs_ are created using `React.createRef()` method and attached to React elements via the `ref` attribute. In order to use _refs_ throughout the component, just assign the _ref_ to the instance property within constructor.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">myRef</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createRef</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.myRef}</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

2. You can also use ref callbacks approach regardless of React version. For example, the search bar component's input element is accessed as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">SearchBar</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">txtSearch</span> = <span class="hljs-literal">null</span>;
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = { <span class="hljs-attr">term</span>: <span class="hljs-string">''</span> };
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">setInputSearchRef</span> = <span class="hljs-function">(<span class="hljs-params">e</span>) =></span> {
            <span class="hljs-variable language_">this</span>.<span class="hljs-property">txtSearch</span> = e;
        };
    }
    <span class="hljs-title function_">onInputChange</span>(<span class="hljs-params">event</span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ <span class="hljs-attr">term</span>: <span class="hljs-variable language_">this</span>.<span class="hljs-property">txtSearch</span>.<span class="hljs-property">value</span> });
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{this.state.term}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{this.onInputChange.bind(this)}</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.setInputSearchRef}</span> /></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

You can also use _refs_ in function components using **closures**.

**Note**: You can also use inline ref callbacks even though it is not a recommended approach.

========== Id ==========  
276

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#276-How-to-create-refs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
