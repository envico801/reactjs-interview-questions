========== Question ==========  

### What are the possible ways of updating objects in state?  

========== Answer ==========  

1.  **Calling `setState()` with an object to merge with state:**

    -   Using `Object.assign()` to create a copy of the object:

        <!-- codeblock-start -->
        <pre><code class="hljs language-javascript">
                <span class="hljs-keyword">const</span> user = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">assign</span>({}, <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">user</span>, { <span class="hljs-attr">age</span>: <span class="hljs-number">42</span> });
                <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ user });
                </code></pre>
        <!-- codeblock-end -->

    -   Using _spread operator_:

        <!-- codeblock-start -->
        <pre><code class="hljs language-javascript">
                <span class="hljs-keyword">const</span> user = { ...<span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span>.<span class="hljs-property">user</span>, <span class="hljs-attr">age</span>: <span class="hljs-number">42</span> };
                <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({ user });
                </code></pre>
        <!-- codeblock-end -->

2.  **Calling `setState()` with a function:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>(<span class="hljs-function">(<span class="hljs-params">prevState</span>) =></span> ({
            <span class="hljs-attr">user</span>: {
                ...prevState.<span class="hljs-property">user</span>,
                <span class="hljs-attr">age</span>: <span class="hljs-number">42</span>,
            },
        }));
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
310

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#310-What-are-the-possible-ways-of-updating-obj

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
