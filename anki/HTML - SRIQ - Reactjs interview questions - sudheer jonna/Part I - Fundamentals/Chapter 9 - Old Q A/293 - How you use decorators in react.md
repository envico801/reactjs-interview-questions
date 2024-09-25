========== Question ==========  

### How you use decorators in React?  

========== Answer ==========  

You can _decorate_ your _class_ components, which is the same as passing the component into a function. **Decorators** are flexible and readable way of modifying component functionality.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">@<span class="hljs-title function_">setTitle</span>(<span class="hljs-string">'Profile'</span>)
<span class="hljs-keyword">class</span> <span class="hljs-title class_">Profile</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-comment">//....</span>
}
<span class="hljs-comment">/*
  title is a string that will be set as a document title
  WrappedComponent is what our decorator will receive when
  put directly above a component class as seen in the example above
*/</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">setTitle</span> = (<span class="hljs-params">title</span>) => <span class="hljs-function">(<span class="hljs-params">WrappedComponent</span>) =></span> {
    <span class="hljs-keyword">return</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">extends</span> <span class="hljs-title class_">React</span>.<span class="hljs-property">Component</span> {
        <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
            <span class="hljs-variable language_">document</span>.<span class="hljs-property">title</span> = title;
        }
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">WrappedComponent</span> {<span class="hljs-attr">...this.props</span>} /></span></span>;
        }
    };
};
</code></pre>
<!-- codeblock-end -->

**Note:** Decorators are a feature that didn't make it into ES7, but are currently a _stage 2 proposal_.

========== Id ==========  
293

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#293-How-you-use-decorators-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
