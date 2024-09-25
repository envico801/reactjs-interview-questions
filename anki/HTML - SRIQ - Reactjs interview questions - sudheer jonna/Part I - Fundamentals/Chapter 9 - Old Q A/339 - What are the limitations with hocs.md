========== Question ==========  

### What are the limitations with HOCs?  

========== Answer ==========  

Higher-order components come with a few caveats apart from its benefits. Below are the few listed in an order,

1.  **Don’t use HOCs inside the render method:**

    It is not recommended to apply a HOC to a component within the render method of a component.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
          <span class="hljs-comment">// A new version of EnhancedComponent is created on every render</span>
          <span class="hljs-comment">// EnhancedComponent1 !== EnhancedComponent2</span>
          <span class="hljs-keyword">const</span> <span class="hljs-title class_">EnhancedComponent</span> = <span class="hljs-title function_">enhance</span>(<span class="hljs-title class_">MyComponent</span>);
          <span class="hljs-comment">// That causes the entire subtree to unmount/remount each time!</span>
          <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">EnhancedComponent</span> /></span></span>;
        }
        </code></pre>
    <!-- codeblock-end -->

    The above code impacts on performance by remounting a component that causes the state of that component and all of its children to be lost. Instead, apply HOCs outside the component definition so that the resulting component is created only once.

2.  **Static methods must be copied over:**

    When you apply a HOC to a component the new component does not have any of the static methods of the original component

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-comment">// Define a static method</span>
        <span class="hljs-title class_">WrappedComponent</span>.<span class="hljs-property">staticMethod</span> = <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
            <span class="hljs-comment">/*...*/</span>
        };
        <span class="hljs-comment">// Now apply a HOC</span>
        <span class="hljs-keyword">const</span> <span class="hljs-title class_">EnhancedComponent</span> = <span class="hljs-title function_">enhance</span>(<span class="hljs-title class_">WrappedComponent</span>);
        <span class="hljs-comment">// The enhanced component has no static method</span>
        <span class="hljs-keyword">typeof</span> <span class="hljs-title class_">EnhancedComponent</span>.<span class="hljs-property">staticMethod</span> === <span class="hljs-string">'undefined'</span>; <span class="hljs-comment">// true</span>
        </code></pre>
    <!-- codeblock-end -->

    You can overcome this by copying the methods onto the container before returning it,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">function</span> <span class="hljs-title function_">enhance</span>(<span class="hljs-params">WrappedComponent</span>) {
            <span class="hljs-keyword">class</span> <span class="hljs-title class_">Enhance</span> <span class="hljs-keyword">extends</span> <span class="hljs-title class_ inherited__">React.Component</span> {
                <span class="hljs-comment">/*...*/</span>
            }
            <span class="hljs-comment">// Must know exactly which method(s) to copy :(</span>
            <span class="hljs-title class_">Enhance</span>.<span class="hljs-property">staticMethod</span> = <span class="hljs-title class_">WrappedComponent</span>.<span class="hljs-property">staticMethod</span>;
            <span class="hljs-keyword">return</span> <span class="hljs-title class_">Enhance</span>;
        }
        </code></pre>
    <!-- codeblock-end -->

3.  **Refs aren’t passed through:**

    For HOCs you need to pass through all props to the wrapped component but this does not work for refs. This is because ref is not really a prop similar to key. In this case you need to use the React.forwardRef API

========== Id ==========  
339

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#339-What-are-the-limitations-with-hocs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
