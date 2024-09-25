========== Question ==========  

### What are uncontrolled components?  

========== Answer ==========  

The **Uncontrolled Components** are the ones that store their own state internally, and you query the DOM using a ref to find its current value when you need it. This is a bit more like traditional HTML.

The uncontrolled components will be implemented using the below steps,

1. Create a ref using useRef react hook in function component or `React.createRef()` in class based component.

2. Attach this ref to the form element.

3. The form element value can be accessed directly through `ref` in event handlers or `componentDidMount` for class components

In the below UserProfile component, the `username` input is accessed using ref.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { useRef } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">UserProfile</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> usernameRef = <span class="hljs-title function_">useRef</span>(<span class="hljs-literal">null</span>);
    <span class="hljs-keyword">const</span> <span class="hljs-title function_">handleSubmit</span> = (<span class="hljs-params">event</span>) => {
        event.<span class="hljs-title function_">preventDefault</span>();
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-string">'The submitted username is: '</span> + usernameRef.<span class="hljs-property">current</span>.<span class="hljs-property">value</span>);
    };
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">onSubmit</span>=<span class="hljs-string">{handleSubmit}</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Username:
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'text'</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{usernameRef}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'submit'</span>></span>Submit<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

In most cases, it's recommend to use controlled components to implement forms. In a controlled component, form data is handled by a React component. The alternative is uncontrolled components, where form data is handled by the DOM itself.

<details><summary><b>See Class</b></summary>

<p>

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">class</span> <span class="hljs-title class_">UserProfile</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
        <span class="hljs-variable language_">super</span>(props);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleSubmit</span> = <span class="hljs-variable language_">this</span>.<span class="hljs-property">handleSubmit</span>.<span class="hljs-title function_">bind</span>(<span class="hljs-variable language_">this</span>);
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">input</span> = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">createRef</span>();
    }
    <span class="hljs-title function_">handleSubmit</span>(<span class="hljs-params">event</span>) {
        <span class="hljs-title function_">alert</span>(<span class="hljs-string">'A name was submitted: '</span> + <span class="hljs-variable language_">this</span>.<span class="hljs-property">input</span>.<span class="hljs-property">current</span>.<span class="hljs-property">value</span>);
        event.<span class="hljs-title function_">preventDefault</span>();
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">onSubmit</span>=<span class="hljs-string">{this.handleSubmit}</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                    {'Name:'}
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'text'</span> <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.input}</span> /></span>
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">'submit'</span> <span class="hljs-attr">value</span>=<span class="hljs-string">'Submit'</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

</p>

</details>

========== Id ==========  
22

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#22-What-are-uncontrolled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
