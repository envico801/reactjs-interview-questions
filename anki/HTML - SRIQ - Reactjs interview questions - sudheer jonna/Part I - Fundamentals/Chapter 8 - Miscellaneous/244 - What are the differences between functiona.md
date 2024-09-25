========== Question ==========  

### What are the differences between Functional and Class Components?  

========== Answer ==========  

There are two different ways to create components in ReactJS. The main differences are listed down as below,

#### 1. Syntax:

The class components uses ES6 classes to create the components. It uses `render` function to display the HTML content in the webpage.

The syntax for class component looks like as below.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>This is a class component<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
    }
}
</code></pre>
<!-- codeblock-end -->

**Note:** The **Pascal Case** is the recommended approach to provide naming to a component.

Functional component has been improved over the years with some added features like Hooks. Here is a syntax for functional component.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'App'</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Hello, I'm a function component<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

#### 2. State:

State contains information or data about a component which may change over time.

In class component, you can update the state when a user interacts with it or server updates the data using the `setState()` method. The initial state is going to be assigned in the `Constructor()` method using the `this.state` object and it is possible to assign different data types such as string, boolean, numbers, etc.

**A simple example showing how we use the setState() and constructor():**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">class</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">Component</span> {
    <span class="hljs-title function_">constructor</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">super</span>();
        <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
            <span class="hljs-attr">message</span>: <span class="hljs-string">'This is a class component'</span>,
        };
    }
    <span class="hljs-title function_">updateMessage</span>(<span class="hljs-params"></span>) {
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
            <span class="hljs-attr">message</span>: <span class="hljs-string">'Updating the class component'</span>,
        });
    }
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{this.state.message}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
                    <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> {
                        this.updateMessage();
                    }}
                >
                    Click!!
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;/></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

You didn't use state in functional components because it was only supported in class components. But over the years hooks have been implemented in functional components which enables to use state too.

The `useState()` hook can used to implement state in functional components. It returns an array with two items: the first item is current state and the next one is a function (setState) that updates the value of the current state.

Let's see an example to demonstrate the state in functional components,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [message, setMessage] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'This is a functional component'</span>);
    <span class="hljs-keyword">const</span> <span class="hljs-title function_">updateMessage</span> = (<span class="hljs-params"></span>) => {
        <span class="hljs-title function_">setMessage</span>(<span class="hljs-string">'Updating the functional component'</span>);
    };
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'App'</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{message} <span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{updateMessage}</span>></span>Click me!!<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

#### 3. Props:

Props are referred to as "properties". The props are passed into React component just like arguments passed to a function. In other words, they are similar to HTML attributes.

The props are accessible in child class component using `this.props` as shown in below example,

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">class</span> <span class="hljs-title class_">Child</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span> This is a functional component and component name is {this.props.name} <span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
    }
}
<span class="hljs-keyword">class</span> <span class="hljs-title class_">Parent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'Parent'</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Child</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'First child component'</span> /></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">Child</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'Second child component'</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

Props in functional components are similar to that of the class components but the difference is the absence of 'this' keyword.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">function</span> <span class="hljs-title function_">Child</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>This is a child component and the component name is{props.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span></span>;
}
<span class="hljs-keyword">function</span> <span class="hljs-title function_">Parent</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">'Parent'</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Child</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'First child component'</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Child</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'Second child component'</span> /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
244

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#244-What-are-the-differences-between-functiona

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
