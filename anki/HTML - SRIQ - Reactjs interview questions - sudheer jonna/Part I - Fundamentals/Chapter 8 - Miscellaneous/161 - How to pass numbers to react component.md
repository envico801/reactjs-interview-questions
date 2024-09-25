========== Question ==========  

### How to pass numbers to React component?  

========== Answer ==========  

We can pass `numbers` as `props` to React component using curly braces `{}` where as `strings` in double quotes `""` or single quotes `''`

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ChildComponent</span> = (<span class="hljs-params">{ name, age }</span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            My Name is {name} and Age is {age}
        <span class="hljs-tag">&#x3C;/></span></span>
    );
};
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ParentComponent</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">ChildComponent</span> <span class="hljs-attr">name</span>=<span class="hljs-string">'Chetan'</span> <span class="hljs-attr">age</span>=<span class="hljs-string">{30}</span> /></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">ParentComponent</span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
161

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#161-How-to-pass-numbers-to-react-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
