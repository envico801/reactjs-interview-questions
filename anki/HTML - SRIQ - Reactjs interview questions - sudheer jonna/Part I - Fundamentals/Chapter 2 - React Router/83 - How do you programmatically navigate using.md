========== Question ==========  

### How do you programmatically navigate using React Router v4?  

========== Answer ==========  

There are three different ways to achieve programmatic routing/navigation within components.

1.  **Using the `withRouter()` higher-order function:**

    The `withRouter()` higher-order function will inject the history object as a prop of the component. This object provides `push()` and `replace()` methods to avoid the usage of context.

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">import</span> { withRouter } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router-dom'</span>; <span class="hljs-comment">// this also works with 'react-router-native'</span>
        <span class="hljs-keyword">const</span> <span class="hljs-title class_">Button</span> = <span class="hljs-title function_">withRouter</span>(<span class="hljs-function">(<span class="hljs-params">{ history }</span>) =></span> (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
                <span class="hljs-attr">type</span>=<span class="hljs-string">'button'</span>
                <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> {
                    history.push('/new-location');
                }}
            >
                {'Click Me!'}
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
        ));
        </code></pre>
    <!-- codeblock-end -->

2.  **Using `<Route>` component and render props pattern:**

    The `<Route>` component passes the same props as `withRouter()`, so you will be able to access the history methods through the history prop.

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">import</span> { <span class="hljs-title class_">Route</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-router-dom'</span>;
        <span class="hljs-keyword">const</span> <span class="hljs-title function_">Button</span> = (<span class="hljs-params"></span>) => (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Route</span>
                <span class="hljs-attr">render</span>=<span class="hljs-string">{({</span> <span class="hljs-attr">history</span> }) =></span> (
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
                        <span class="hljs-attr">type</span>=<span class="hljs-string">'button'</span>
                        <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> {
                            history.push('/new-location');
                        }}
                    >
                        {'Click Me!'}
                    <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
                )}
            /></span>
        );
        </code></pre>
    <!-- codeblock-end -->

3.  **Using context:**

    This option is not recommended and treated as unstable API.

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        <span class="hljs-keyword">const</span> <span class="hljs-title function_">Button</span> = (<span class="hljs-params">props, context</span>) => (
            <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
                <span class="hljs-attr">type</span>=<span class="hljs-string">'button'</span>
                <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> {
                    context.history.push('/new-location');
                }}
            >
                {'Click Me!'}
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
        );
        <span class="hljs-title class_">Button</span>.<span class="hljs-property">contextTypes</span> = {
            <span class="hljs-attr">history</span>: <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-title function_">shape</span>({
                <span class="hljs-attr">push</span>: <span class="hljs-title class_">React</span>.<span class="hljs-property">PropTypes</span>.<span class="hljs-property">func</span>.<span class="hljs-property">isRequired</span>,
            }),
        };
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
83

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 2 - React Router

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-2-React-Router::#83-How-do-you-programmatically-navigate-using

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
