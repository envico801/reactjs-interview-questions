========== Question ==========  

### How do you use contextType?  

========== Answer ==========  

ContextType is used to consume the context object. The contextType property can be used in two ways,

1.  **contextType as property of class:**

    The contextType property on a class can be assigned a Context object created by React.createContext(). After that, you can consume the nearest current value of that Context type using this.context in any of the lifecycle methods and render function.

    Lets assign contextType property on MyClass as below,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyClass</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">let</span> value = <span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>;
                <span class="hljs-comment">/* perform a side-effect at mount using the value of MyContext */</span>
            }
            <span class="hljs-title function_">componentDidUpdate</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">let</span> value = <span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>;
                <span class="hljs-comment">/* ... */</span>
            }
            <span class="hljs-title function_">componentWillUnmount</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">let</span> value = <span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>;
                <span class="hljs-comment">/* ... */</span>
            }
            <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">let</span> value = <span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>;
                <span class="hljs-comment">/* render something based on the value of MyContext */</span>
            }
        }
        <span class="hljs-title class_">MyClass</span>.<span class="hljs-property">contextType</span> = <span class="hljs-title class_">MyContext</span>;
        </code></pre>
    <!-- codeblock-end -->

2.  **Static field**

    You can use a static class field to initialize your contextType using public class field syntax.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">class</span> <span class="hljs-title class_">MyClass</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-keyword">static</span> contextType = <span class="hljs-title class_">MyContext</span>;
            <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">let</span> value = <span class="hljs-variable language_">this</span>.<span class="hljs-property">context</span>;
                <span class="hljs-comment">/* render something based on the value */</span>
            }
        }
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
346

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#346-How-do-you-use-contexttype

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
