========== Question ==========  

### What are the two ways of formatting in React Intl?  

========== Answer ==========  

The library provides two ways to format strings, numbers, and dates:

1.  **Using react components:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">        &#x3C;<span class="hljs-title class_">FormattedMessage</span> id={<span class="hljs-string">'account'</span>} defaultMessage={<span class="hljs-string">'The amount is less than minimum balance.'</span>} />
        </code></pre>
    <!-- codeblock-end -->

2.  **Using an API:**

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">const</span> messages = <span class="hljs-title function_">defineMessages</span>({
            <span class="hljs-attr">accountMessage</span>: {
                <span class="hljs-attr">id</span>: <span class="hljs-string">'account'</span>,
                <span class="hljs-attr">defaultMessage</span>: <span class="hljs-string">'The amount is less than minimum balance.'</span>,
            },
        });
        <span class="hljs-title function_">formatMessage</span>(messages.<span class="hljs-property">accountMessage</span>);
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
92

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#92-What-are-the-two-ways-of-formatting-in-rea

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
