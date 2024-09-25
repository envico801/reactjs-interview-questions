========== Question ==========  

### What is the purpose of the constants in Redux?  

========== Answer ==========  

Constants allows you to easily find all usages of that specific functionality across the project when you use an IDE. It also prevents you from introducing silly bugs caused by typos – in which case, you will get a `ReferenceError` immediately.

Normally we will save them in a single file (`constants.js` or `actionTypes.js`).

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">ADD_TODO</span> = <span class="hljs-string">'ADD_TODO'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">DELETE_TODO</span> = <span class="hljs-string">'DELETE_TODO'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">EDIT_TODO</span> = <span class="hljs-string">'EDIT_TODO'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">COMPLETE_TODO</span> = <span class="hljs-string">'COMPLETE_TODO'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">COMPLETE_ALL</span> = <span class="hljs-string">'COMPLETE_ALL'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">const</span> <span class="hljs-variable constant_">CLEAR_COMPLETED</span> = <span class="hljs-string">'CLEAR_COMPLETED'</span>;
</code></pre>
<!-- codeblock-end -->

In Redux, you use them in two places:

1.  **During action creation:**

    Let's take `actions.js`:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> { <span class="hljs-variable constant_">ADD_TODO</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./actionTypes'</span>;
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">addTodo</span>(<span class="hljs-params">text</span>) {
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">type</span>: <span class="hljs-variable constant_">ADD_TODO</span>, text };
        }
        </code></pre>
    <!-- codeblock-end -->

2.  **In reducers:**

    Let's create `reducer.js`:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> { <span class="hljs-variable constant_">ADD_TODO</span> } <span class="hljs-keyword">from</span> <span class="hljs-string">'./actionTypes'</span>;
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> (state = [], action) => {
            <span class="hljs-keyword">switch</span> (action.<span class="hljs-property">type</span>) {
                <span class="hljs-keyword">case</span> <span class="hljs-attr">ADD_TODO</span>:
                    <span class="hljs-keyword">return</span> [
                        ...state,
                        {
                            <span class="hljs-attr">text</span>: action.<span class="hljs-property">text</span>,
                            <span class="hljs-attr">completed</span>: <span class="hljs-literal">false</span>,
                        },
                    ];
                <span class="hljs-attr">default</span>:
                    <span class="hljs-keyword">return</span> state;
            }
        };
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
118

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#118-What-is-the-purpose-of-the-constants-in-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
