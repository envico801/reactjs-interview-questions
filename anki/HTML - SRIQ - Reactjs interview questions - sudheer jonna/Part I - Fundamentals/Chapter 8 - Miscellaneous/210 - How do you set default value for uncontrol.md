========== Question ==========  

### How do you set default value for uncontrolled component?  

========== Answer ==========  

In React, the value attribute on form elements will override the value in the DOM. With an uncontrolled component, you might want React to specify the initial value, but leave subsequent updates uncontrolled. To handle this case, you can specify a **defaultValue** attribute instead of **value**.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">render</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">return</span> (
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">form</span> <span class="hljs-attr">onSubmit</span>=<span class="hljs-string">{this.handleSubmit}</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
        User Name:
        <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span>
          <span class="hljs-attr">defaultValue</span>=<span class="hljs-string">"John"</span>
          <span class="hljs-attr">type</span>=<span class="hljs-string">"text"</span>
          <span class="hljs-attr">ref</span>=<span class="hljs-string">{this.input}</span> /></span>
      <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
      <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">type</span>=<span class="hljs-string">"submit"</span> <span class="hljs-attr">value</span>=<span class="hljs-string">"Submit"</span> /></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">form</span>></span></span>
  );
}
</code></pre>
<!-- codeblock-end -->

The same applies for `select` and `textArea` inputs. But you need to use **defaultChecked** for `checkbox` and `radio` inputs.

========== Id ==========  
210

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#210-How-do-you-set-default-value-for-uncontrol

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
