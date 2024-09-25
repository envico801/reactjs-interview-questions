========== Question ==========  

### How to apply validation on props in React?  

========== Answer ==========  

When the application is running in _development mode_, React will automatically check all props that we set on components to make sure they have _correct type_. If the type is incorrect, React will generate warning messages in the console. It's disabled in _production mode_ due to performance impact. The mandatory props are defined with `isRequired`.

The set of predefined prop types:

1. `PropTypes.number`

2. `PropTypes.string`

3. `PropTypes.array`

4. `PropTypes.object`

5. `PropTypes.func`

6. `PropTypes.node`

7. `PropTypes.element`

8. `PropTypes.bool`

9. `PropTypes.symbol`

10. `PropTypes.any`

We can define `propTypes` for `User` component as below:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">PropTypes</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'prop-types'</span>;
<span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
    <span class="hljs-keyword">static</span> propTypes = {
        <span class="hljs-attr">name</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">string</span>.<span class="hljs-property">isRequired</span>,
        <span class="hljs-attr">age</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">number</span>.<span class="hljs-property">isRequired</span>,
    };
    <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
        <span class="hljs-keyword">return</span> (
            <span class="xml"><span class="hljs-tag">&#x3C;></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{`Welcome, ${this.props.name}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{`Age, ${this.props.age}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
            <span class="hljs-tag">&#x3C;/></span></span>
        );
    }
}
</code></pre>
<!-- codeblock-end -->

**Note:** In React v15.5 _PropTypes_ were moved from `React.PropTypes` to `prop-types` library.

_The Equivalent Functional Component_

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">PropTypes</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'prop-types'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">User</span>(<span class="hljs-params">{ name, age }</span>) {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>{`Welcome, ${name}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>{`Age, ${age}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
<span class="hljs-title class_">User</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">name</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">string</span>.<span class="hljs-property">isRequired</span>,
    <span class="hljs-attr">age</span>: <span class="hljs-title class_">PropTypes</span>.<span class="hljs-property">number</span>.<span class="hljs-property">isRequired</span>,
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
36

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#36-How-to-apply-validation-on-props-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
