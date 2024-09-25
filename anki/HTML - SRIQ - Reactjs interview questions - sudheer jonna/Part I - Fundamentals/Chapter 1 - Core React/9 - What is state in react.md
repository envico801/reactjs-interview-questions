========== Question ==========  

### What is state in React?  

========== Answer ==========  

_State_ of a component is an object that holds some information that may change over the lifetime of the component. The important point is whenever the state object changes, the component re-renders. It is always recommended to make our state as simple as possible and minimize the number of stateful components.

![state](../../../../images/state.jpg)

Let's take an example of **User** component with `message` state. Here, **useState** hook has been used to add state to the User component and it returns an array with current state and function to update it.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">User</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [message, setMessage] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'Welcome to React world'</span>);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{message}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

Whenever React calls your component or access `useState` hook, it gives you a snapshot of the state for that particular render.

<details><summary><b>See Class</b></summary>

<p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">message</span>: <span class="hljs-string">'Welcome to React world'</span>,
        };
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{this.state.message}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

</p>

</details>

State is similar to props, but it is private and fully controlled by the component ,i.e., it is not accessible to any other component till the owner component decides to pass it.

========== Id ==========  
9

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#9-What-is-state-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
