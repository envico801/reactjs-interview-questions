========== Question ==========  

### Can you describe about componentDidCatch lifecycle method signature?  

========== Answer ==========  

The **componentDidCatch** lifecycle method is invoked after an error has been thrown by a descendant component. The method receives two parameters,

1.  error: - The error object which was thrown

2.  info: - An object with a componentStack key contains the information about which component threw the error.

The method structure would be as follows

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-title function_">componentDidCatch</span>(error, info);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
173

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#173-Can-you-describe-about-componentdidcatch-l

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
