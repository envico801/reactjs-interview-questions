========== Question ==========  

### How to make AJAX call and in which component lifecycle methods should I make an AJAX call?  

========== Answer ==========  

You can use AJAX libraries such as Axios, jQuery AJAX, and the browser built-in `fetch`. You should fetch data in the `componentDidMount()` lifecycle method. This is so you can use `setState()` to update your component when the data is retrieved.

For example, the employees list fetched from API and set local state:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">MyComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">employees</span>: [],
            <span class="hljs-attr">error</span>: <span class="hljs-literal">null</span>,
        };
    }
    <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
        <span class="hljs-title function_">fetch</span>(<span class="hljs-string">'https://api.example.com/items'</span>)
            .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">res</span>) =></span> res.<span class="hljs-title function_">json</span>())
            .<span class="hljs-title function_">then</span>(
                <span class="hljs-function">(<span class="hljs-params">result</span>) =></span> {
                    <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
                        <span class="hljs-attr">employees</span>: result.<span class="hljs-property">employees</span>,
                    });
                },
                <span class="hljs-function">(<span class="hljs-params">error</span>) =></span> {
                    <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ error });
                },
            );
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">const</span> { error, employees } = <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>;
        <span class="hljs-keyword">if</span> (error) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>Error: {error.message}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
        } <span class="hljs-keyword">else</span> {
            <span class="hljs-keyword">return</span> (
                <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
                    {employees.map((employee) => (
                        <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{employee.name}</span>></span>
                            {employee.name}-{employee.experience}
                        <span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
                    ))}
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
            );
        }
    }
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
318

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#318-How-to-make-ajax-call-and-in-which-compone

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
