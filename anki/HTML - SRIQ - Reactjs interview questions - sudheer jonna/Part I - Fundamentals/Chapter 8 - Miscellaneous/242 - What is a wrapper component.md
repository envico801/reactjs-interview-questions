========== Question ==========  

### What is a wrapper component?  

========== Answer ==========  

A wrapper in React is a component that wraps or surrounds another component or group of components. It can be used for a variety of purposes such as adding additional functionality, styling, or layout to the wrapped components.

For example, consider a simple component that displays a message:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">Message</span> = (<span class="hljs-params">{ text }</span>) => {
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>{text}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span></span>;
};
</code></pre>
<!-- codeblock-end -->

We can create a wrapper component that will add a border to the message component:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">MessageWrapper</span> = (<span class="hljs-params">props</span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">style</span>=<span class="hljs-string">{{</span> <span class="hljs-attr">border:</span> '<span class="hljs-attr">1px</span> <span class="hljs-attr">solid</span> <span class="hljs-attr">black</span>' }}></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Message</span> {<span class="hljs-attr">...props</span>} /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
</code></pre>
<!-- codeblock-end -->

Now we can use the MessageWrapper component instead of the Message component and the message will be displayed with a border:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">MessageWrapper</span> text=<span class="hljs-string">'Hello World'</span> />
</code></pre>
<!-- codeblock-end -->

Wrapper component can also accept its own props and pass them down to the wrapped component, for example, we can create a wrapper component that will add a title to the message component:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title function_">MessageWrapperWithTitle</span> = (<span class="hljs-params">{ title, ...props }</span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">h3</span>></span>{title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">h3</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">Message</span> {<span class="hljs-attr">...props</span>} /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
</code></pre>
<!-- codeblock-end -->

Now we can use the MessageWrapperWithTitle component and pass title props:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;<span class="hljs-title class_">MessageWrapperWithTitle</span> title=<span class="hljs-string">'My Message'</span> text=<span class="hljs-string">'Hello World'</span> />
</code></pre>
<!-- codeblock-end -->

This way, the wrapper component can add additional functionality, styling, or layout to the wrapped component while keeping the wrapped component simple and reusable.

========== Id ==========  
242

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#242-What-is-a-wrapper-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
