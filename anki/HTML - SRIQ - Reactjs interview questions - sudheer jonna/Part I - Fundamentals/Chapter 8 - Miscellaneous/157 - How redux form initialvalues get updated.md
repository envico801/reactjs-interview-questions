========== Question ==========  

### How Redux Form `initialValues` get updated from state?  

========== Answer ==========  

You need to add `enableReinitialize : true` setting.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> <span class="hljs-title class_">InitializeFromStateForm</span> = <span class="hljs-title function_">reduxForm</span>({
    <span class="hljs-attr">form</span>: <span class="hljs-string">'initializeFromState'</span>,
    <span class="hljs-attr">enableReinitialize</span>: <span class="hljs-literal">true</span>,
})(<span class="hljs-title class_">UserEdit</span>);
</code></pre>
<!-- codeblock-end -->

If your `initialValues` prop gets updated, your form will update too.

========== Id ==========  
157

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#157-How-redux-form-initialvalues-get-updated

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
