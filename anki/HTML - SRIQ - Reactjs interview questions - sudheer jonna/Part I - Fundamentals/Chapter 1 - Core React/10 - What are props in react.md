========== Question ==========  

### What are props in React?  

========== Answer ==========  

_Props_ are inputs to components. They are single values or objects containing a set of values that are passed to components on creation similar to HTML-tag attributes. Here, the data is passed down from a parent component to a child component.

The primary purpose of props in React is to provide following component functionality:

1. Pass custom data to your component.

2. Trigger state changes.

3. Use via `this.props.reactProp` inside component's `render()` method.

For example, let us create an element with `reactProp` property:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">Element</span> reactProp={<span class="hljs-string">'1'</span>} />
</code></pre>
<!-- codeblock-end -->

This `reactProp` (or whatever you came up with) attribute name then becomes a property attached to React's native props object which originally already exists on all components created using React library.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">props.<span class="hljs-property">reactProp</span>;
</code></pre>
<!-- codeblock-end -->

For example, the usage of props in function component looks like below:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ReactDOM</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ChildComponent</span> = (<span class="hljs-params">props</span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{props.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{props.age}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{props.gender}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ParentComponent</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">ChildComponent</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'John'</span> <span class="hljs-attr">age</span>=<span class="hljs-string">'30'</span> <span class="hljs-attr">gender</span>=<span class="hljs-string">'male'</span> /></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">ChildComponent</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'Mary'</span> <span class="hljs-attr">age</span>=<span class="hljs-string">'25'</span> <span class="hljs-attr">geneder</span>=<span class="hljs-string">'female'</span> /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
</code></pre>
<!-- codeblock-end -->

The properties from props object can be accessed directly using destructing feature from ES6 (ECMAScript 2015). It is also possible to fallback to default value when the prop value is not specified. The above child component can be simplified like below.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">ChildComponent</span> = (<span class="hljs-params">{ name, age, gender = <span class="hljs-string">'male'</span> }</span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{age}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{gender}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
</code></pre>
<!-- codeblock-end -->

**Note:** The default value won't be used if you pass `null` or `0` value. i.e, default value is only used if the prop value is missed or `undefined` value has been passed.

  <details><summary><b>See Class</b></summary>

The Props accessed in Class Based Component as below

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ReactDOM</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom'</span>;
<span class="hljs-keyword">class</span> <span class="hljs-title class_">ChildComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{this.props.name}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{this.props.age}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{this.props.gender}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
<span class="hljs-keyword">class</span> <span class="hljs-title class_">ParentComponent</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">ChildComponent</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'John'</span> <span class="hljs-attr">age</span>=<span class="hljs-string">'30'</span> <span class="hljs-attr">gender</span>=<span class="hljs-string">'male'</span> /></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">ChildComponent</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'Mary'</span> <span class="hljs-attr">age</span>=<span class="hljs-string">'25'</span> <span class="hljs-attr">gender</span>=<span class="hljs-string">'female'</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

  </details>

========== Id ==========  
10

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#10-What-are-props-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
