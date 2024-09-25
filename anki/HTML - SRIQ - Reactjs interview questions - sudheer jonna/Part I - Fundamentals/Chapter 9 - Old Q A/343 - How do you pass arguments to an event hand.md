========== Question ==========  

### How do you pass arguments to an event handler?  

========== Answer ==========  

During iterations or loops, it is common to pass an extra parameter to an event handler. This can be achieved through arrow functions or bind method.

Let us take an example of user details updated in a grid,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;button onClick={<span class="hljs-function">(<span class="hljs-params">e</span>) =></span> <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">updateUser</span>(userId, e)}><span class="hljs-title class_">Update</span> <span class="hljs-title class_">User</span> details&#x3C;/button>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{this.updateUser.bind(this,</span> <span class="hljs-attr">userId</span>)}></span>Update User details<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
</code></pre>
<!-- codeblock-end -->

In the both approaches, the synthetic argument `e` is passed as a second argument. You need to pass it explicitly for arrow functions and it will be passed automatically for `bind` method.

========== Id ==========  
343

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#343-How-do-you-pass-arguments-to-an-event-hand

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
