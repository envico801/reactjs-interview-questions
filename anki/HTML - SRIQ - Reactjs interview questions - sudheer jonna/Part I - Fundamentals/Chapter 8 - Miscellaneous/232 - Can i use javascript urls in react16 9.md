========== Question ==========  

### Can I use javascript urls in react16.9?  

========== Answer ==========  

Yes, you can use javascript: URLs but it will log a warning in the console. Because URLs starting with javascript: are dangerous by including unsanitized output in a tag like `<a href>` and create a security hole.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> companyProfile = {
    <span class="hljs-attr">website</span>: <span class="hljs-string">"javascript: alert('Your website is hacked')"</span>,
};
<span class="hljs-comment">// It will log a warning</span>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">a</span> <span class="hljs-attr">href</span>=<span class="hljs-string">{companyProfile.website}</span>></span>More details<span class="hljs-tag">&#x3C;/<span class="hljs-name">a</span>></span></span>;
</code></pre>
<!-- codeblock-end -->

Remember that the future versions will throw an error for javascript URLs.

========== Id ==========  
232

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#232-Can-i-use-javascript-urls-in-react16-9

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
