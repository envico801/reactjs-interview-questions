========== Question ==========  

### How to prevent component from rendering?  

========== Answer ==========  

You can prevent component from rendering by returning null based on specific condition. This way it can conditionally render component.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Greeting</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">if</span> (!props.<span class="hljs-property">loggedIn</span>) {
        <span class="hljs-keyword">return</span> <span class="hljs-literal">null</span>;
    }
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'greeting'</span>></span>welcome, {props.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-variable language_">super</span>(props);
    <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {<span class="hljs-attr">loggedIn</span>: <span class="hljs-literal">false</span>, <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>};
  }
  <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
   <span class="hljs-keyword">return</span> (
       <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
         //Prevent component render if it is not loggedIn
         <span class="hljs-tag">&#x3C;<span class="hljs-name">Greeting</span> <span class="hljs-attr">loggedIn</span>=<span class="hljs-string">{this.state.loggedIn}</span> /></span>
         <span class="hljs-tag">&#x3C;<span class="hljs-name">UserDetails</span> <span class="hljs-attr">name</span>=<span class="hljs-string">{this.state.name}</span>></span>
       <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
   );
  }

</span></code></pre>
<!-- codeblock-end -->

In the above example, the `greeting` component skips its rendering section by applying condition and returning null value.

========== Id ==========  
344

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#344-How-to-prevent-component-from-rendering

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
