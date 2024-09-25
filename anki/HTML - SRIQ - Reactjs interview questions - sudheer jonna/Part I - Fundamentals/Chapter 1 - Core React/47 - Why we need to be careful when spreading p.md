========== Question ==========  

### Why we need to be careful when spreading props on DOM elements?  

========== Answer ==========  

When we _spread props_ we run into the risk of adding unknown HTML attributes, which is a bad practice. Instead we can use prop destructuring with `...rest` operator, so it will add only required props.

For example,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> <span class="hljs-title function_">ComponentA</span> = (<span class="hljs-params"></span>) => <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ComponentB</span> <span class="hljs-attr">isDisplay</span>=<span class="hljs-string">{true}</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">componentStyle</span>'} /></span></span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ComponentB</span> = (<span class="hljs-params">{ isDisplay, ...domProps }</span>) => <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> {<span class="hljs-attr">...domProps</span>}></span>{'ComponentB'}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
47

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#47-Why-we-need-to-be-careful-when-spreading-p

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
