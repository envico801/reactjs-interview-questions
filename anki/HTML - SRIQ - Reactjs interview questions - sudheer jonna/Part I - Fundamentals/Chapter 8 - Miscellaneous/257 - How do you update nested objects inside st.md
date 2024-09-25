========== Question ==========  

### How do you update nested objects inside state?  

========== Answer ==========  

You cannot simply use spread syntax for all kinds of objects inside state. Because spread syntax is shallow and it copies properties for one level deep only. If the object has nested object structure, UI doesn't work as expected with regular JavaScript nested property mutation. Let's demonstrate this behavior with an example of User object which has address nested object inside of it.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">const</span> user = {
    <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
    <span class="hljs-attr">age</span>: <span class="hljs-number">32</span>,
    <span class="hljs-attr">address</span>: {
        <span class="hljs-attr">country</span>: <span class="hljs-string">'Singapore'</span>,
        <span class="hljs-attr">postalCode</span>: <span class="hljs-number">440004</span>,
    },
};
</code></pre>
<!-- codeblock-end -->

If you try to update the country nested field in a regular javascript fashion(as shown below) then user profile screen won't be updated with latest value.

<!-- codeblock-start -->
<pre><code class="hljs language-js">user.<span class="hljs-property">address</span>.<span class="hljs-property">country</span> = <span class="hljs-string">'Germany'</span>;
</code></pre>
<!-- codeblock-end -->

This issue can be fixed by flattening all the fields into a top-level object or create a new object for each nested object and point it to it's parent object. In this example, first you need to create copy of address object and update it with the latest value. Later, the address object should be linked to parent user object something like below.

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-title function_">setUser</span>({
    ...user,
    <span class="hljs-attr">address</span>: {
        ...user.<span class="hljs-property">address</span>,
        <span class="hljs-attr">country</span>: <span class="hljs-string">'Germany'</span>,
    },
});
</code></pre>
<!-- codeblock-end -->

This approach is bit verbose and not easy for deep hierarchical state updates. But this workaround can be used for few levels of nested objects without much hassle.

========== Id ==========  
257

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#257-How-do-you-update-nested-objects-inside-st

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
