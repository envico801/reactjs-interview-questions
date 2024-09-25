========== Question ==========  

### What are inline conditional expressions?  

========== Answer ==========  

You can use either _if statements_ or _ternary expressions_ which are available from JS to conditionally render expressions. Apart from these approaches, you can also embed any expressions in JSX by wrapping them in curly braces and then followed by JS logical operator `&&`.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">&#x3C;h1><span class="hljs-title class_">Hello</span>!&#x3C;/h1>;
{
    messages.<span class="hljs-property">length</span> > <span class="hljs-number">0</span> &#x26;&#x26; !isLogin ? <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>You have {messages.length} unread messages.<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span></span> : <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">h2</span>></span>You don't have unread messages.<span class="hljs-tag">&#x3C;/<span class="hljs-name">h2</span>></span></span>;
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
14

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#14-What-are-inline-conditional-expressions

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
