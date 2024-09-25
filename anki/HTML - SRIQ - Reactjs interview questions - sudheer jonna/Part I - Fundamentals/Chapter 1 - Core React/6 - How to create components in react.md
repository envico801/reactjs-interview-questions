========== Question ==========  

### How to create components in React?  

========== Answer ==========  

Components are the building blocks of creating User Interfaces(UI) in React. There are two possible ways to create a component.

1. **Function Components:** This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as the one and only one parameter and return React elements to render the output:

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">Greeting</span>(<span class="hljs-params">{ message }</span>) {
            <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{`Hello, ${message}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
        }
        </code></pre>
    <!-- codeblock-end -->

2. **Class Components:** You can also use ES6 class to define a component. The above function component can be written as a class component:

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">class</span> <span class="hljs-title class_">Greeting</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
            <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
                <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{`Hello, ${this.props.message}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
            }
        }
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
6

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#6-How-to-create-components-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
