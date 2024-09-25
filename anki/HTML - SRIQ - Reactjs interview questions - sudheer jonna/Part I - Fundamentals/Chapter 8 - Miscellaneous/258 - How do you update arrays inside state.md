========== Question ==========  

### How do you update arrays inside state?  

========== Answer ==========  

Eventhough arrays in JavaScript are mutable in nature, you need to treat them as immutable while storing them in a state. That means, similar to objects, the arrays cannot be updated directly inside state. Instead, you need to create a copy of the existing array and then set the state to use newly copied array.

To ensure that arrays are not mutated, the mutation operations like direct direct assignment(arr[1]='one'), push, pop, shift, unshift, splice etc methods should be avoided on original array. Instead, you can create a copy of existing array with help of array operations such as filter, map, slice, spread syntax etc.

For example, the below push operation doesn't add the new todo to the total todo's list in an event handler.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">onClick = {
  todos.<span class="hljs-title function_">push</span>({
    <span class="hljs-attr">id</span>: id+<span class="hljs-number">1</span>,
    <span class="hljs-attr">name</span>: name
  })
}
</code></pre>
<!-- codeblock-end -->

This issue is fixed by replacing push operation with spread syntax where it will create a new array and the UI updated with new todo.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx">onClick = {
  [
    ...todos,
    { <span class="hljs-attr">id</span>: id+<span class="hljs-number">1</span>, <span class="hljs-attr">name</span>: name }
  ]
}
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
258

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#258-How-do-you-update-arrays-inside-state

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
