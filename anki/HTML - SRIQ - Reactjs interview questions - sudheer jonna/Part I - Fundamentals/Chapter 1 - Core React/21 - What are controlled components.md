========== Question ==========  

### What are controlled components?  

========== Answer ==========  

A component that controls the input elements within the forms on subsequent user input is called **Controlled Component**, i.e, every state mutation will have an associated handler function. That means, the displayed data is always in sync with the state of the component.

The controlled components will be implemented using the below steps,

1. Initialize the state using use state hooks in function components or inside constructor for class components.

2. Set the value of the form element to the respective state variable.

3. Create an event handler to handle the user input changes through useState updater function or setState from class component.

4. Attach the above event handler to form elements change or click events

For example, the name input field updates the user name using `handleChange` event handler as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">UserProfile</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [username, setUsername] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">''</span>);
    <span class="hljs-keyword">const</span> <span class="hljs-title function_">handleChange</span> = (<span class="hljs-params">e</span>) => {
        <span class="hljs-title function_">setUsername</span>(e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>);
    };
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Name:
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'text'</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{username}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{handleChange}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
21

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#21-What-are-controlled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
