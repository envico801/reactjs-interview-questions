========== Question ==========  

### How to use https instead of http in create-react-app?  

========== Answer ==========  

You just need to use `HTTPS=true` configuration. You can edit your `package.json` scripts section:

<!-- codeblock-start -->
<pre><code class="hljs language-json"><span class="hljs-attr">"scripts"</span><span class="hljs-punctuation">:</span> <span class="hljs-punctuation">{</span>
  <span class="hljs-attr">"start"</span><span class="hljs-punctuation">:</span> <span class="hljs-string">"set HTTPS=true &#x26;&#x26; react-scripts start"</span>
<span class="hljs-punctuation">}</span>
</code></pre>
<!-- codeblock-end -->

or just run `set HTTPS=true && npm start`

========== Id ==========  
312

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#312-How-to-use-https-instead-of-http-in-create

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
