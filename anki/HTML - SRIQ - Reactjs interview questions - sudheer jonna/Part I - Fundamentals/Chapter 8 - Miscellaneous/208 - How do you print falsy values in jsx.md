========== Question ==========  

### How do you print falsy values in JSX?  

========== Answer ==========  

The falsy values such as false, null, undefined, and true are valid children but they don't render anything. If you still want to display them then you need to convert it to string. Let's take an example on how to convert to a string,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;div><span class="hljs-title class_">My</span> <span class="hljs-title class_">JavaScript</span> variable is {<span class="hljs-title class_">String</span>(myVariable)}.&#x3C;/div>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
208

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#208-How-do-you-print-falsy-values-in-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
