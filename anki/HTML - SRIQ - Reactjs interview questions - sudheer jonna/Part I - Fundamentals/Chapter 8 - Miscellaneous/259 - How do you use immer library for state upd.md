========== Question ==========  

### How do you use immer library for state updates?  

========== Answer ==========  

Immer library enforces the immutability of state based on **copy-on-write** mechanism. It uses JavaScript proxy to keep track of updates to immutable states. Immer has 3 main states as below,

1. **Current state:** It refers to actual state

2. **Draft state:** All new changes will be applied to this state. In this state, draft is just a proxy of the current state.

3. **Next state:** It is formed after all mutations applied to the draft state

Immer can be used by following below instructions,

1. Install the dependency using `npm install use-immer` command

2. Replace `useState` hook with `useImmer` hook by importing at the top

3. The setter function of `useImmer` hook can be used to update the state.

For example, the mutation syntax of immer library simplifies the nested address object of user state as follows,

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { useImmer } <span class="hljs-keyword">from</span> <span class="hljs-string">'use-immer'</span>;
<span class="hljs-keyword">const</span> [user, setUser] = <span class="hljs-title function_">useImmer</span>({
    <span class="hljs-attr">name</span>: <span class="hljs-string">'John'</span>,
    <span class="hljs-attr">age</span>: <span class="hljs-number">32</span>,
    <span class="hljs-attr">address</span>: {
        <span class="hljs-attr">country</span>: <span class="hljs-string">'Singapore'</span>,
        <span class="hljs-attr">postalCode</span>: <span class="hljs-number">440004</span>,
    },
});
<span class="hljs-comment">//Update user details upon any event</span>
<span class="hljs-title function_">setUser</span>(<span class="hljs-function">(<span class="hljs-params">draft</span>) =></span> {
    draft.<span class="hljs-property">address</span>.<span class="hljs-property">country</span> = <span class="hljs-string">'Germany'</span>;
});
</code></pre>
<!-- codeblock-end -->

The preceding code enables you to update nested objects with a conceise mutation syntax.

========== Id ==========  
259

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#259-How-do-you-use-immer-library-for-state-upd

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
