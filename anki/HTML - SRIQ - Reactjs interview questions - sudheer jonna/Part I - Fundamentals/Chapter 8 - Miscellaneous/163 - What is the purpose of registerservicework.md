========== Question ==========  

### What is the purpose of registerServiceWorker in React?  

========== Answer ==========  

React creates a service worker for you without any configuration by default. The service worker is a web API that helps you cache your assets and other files so that when the user is offline or on a slow network, he/she can still see results on the screen, as such, it helps you build a better user experience, that's what you should know about service worker for now. It's all about adding offline capabilities to your site.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ReactDOM</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./App'</span>;
<span class="hljs-keyword">import</span> registerServiceWorker <span class="hljs-keyword">from</span> <span class="hljs-string">'./registerServiceWorker'</span>;
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span></span>, <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'root'</span>));
<span class="hljs-title function_">registerServiceWorker</span>();
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
163

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#163-What-is-the-purpose-of-registerservicework

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
