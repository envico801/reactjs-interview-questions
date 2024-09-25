========== Question ==========  

### Give an example of Styled Components?  

========== Answer ==========  

Lets create `<Title>` and `<Wrapper>` components with specific styles for each.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> styled <span class="hljs-keyword">from</span> <span class="hljs-string">'styled-components'</span>;
<span class="hljs-comment">// Create a &#x3C;Title> component that renders an &#x3C;h1> which is centered, red and sized at 1.5em</span>
<span class="hljs-keyword">const</span> <span class="hljs-title class_">Title</span> = styled.<span class="hljs-property">h1</span><span class="hljs-string">`
    font-size: 1.5em;
    text-align: center;
    color: palevioletred;
`</span>;
<span class="hljs-comment">// Create a &#x3C;Wrapper> component that renders a &#x3C;section> with some padding and a papayawhip background</span>
<span class="hljs-keyword">const</span> <span class="hljs-title class_">Wrapper</span> = styled.<span class="hljs-property">section</span><span class="hljs-string">`
    padding: 4em;
    background: papayawhip;
`</span>;
</code></pre>
<!-- codeblock-end -->

These two variables, `Title` and `Wrapper`, are now components that you can render just like any other react component.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;<span class="hljs-title class_">Wrapper</span>>
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">Title</span>></span>{'Lets start first styled component!'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">Title</span>></span></span>
&#x3C;/<span class="hljs-title class_">Wrapper</span>>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
151

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#151-Give-an-example-of-styled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
