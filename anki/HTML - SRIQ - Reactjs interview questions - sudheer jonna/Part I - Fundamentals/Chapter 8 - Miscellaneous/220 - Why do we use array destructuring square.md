========== Question ==========  

### Why do we use array destructuring (square brackets notation) in `useState`?  

========== Answer ==========  

When we declare a state variable with `useState`, it returns a pair — an array with two items. The first item is the current value, and the second is a function that updates the value. Using [0] and [1] to access them is a bit confusing because they have a specific meaning. This is why we use array destructuring instead.

For example, the array index access would look as follows:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> userStateVariable = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'userProfile'</span>); <span class="hljs-comment">// Returns an array pair</span>
<span class="hljs-keyword">var</span> user = userStateVariable[<span class="hljs-number">0</span>]; <span class="hljs-comment">// Access first item</span>
<span class="hljs-keyword">var</span> setUser = userStateVariable[<span class="hljs-number">1</span>]; <span class="hljs-comment">// Access second item</span>
</code></pre>
<!-- codeblock-end -->

Whereas with array destructuring the variables can be accessed as follows:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> [user, setUser] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'userProfile'</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
220

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#220-Why-do-we-use-array-destructuring-square

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
