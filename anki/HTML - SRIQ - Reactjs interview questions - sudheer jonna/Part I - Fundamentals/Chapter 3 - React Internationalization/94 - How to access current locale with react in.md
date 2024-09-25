========== Question ==========  

### How to access current locale with React Intl?  

========== Answer ==========  

You can get the current locale in any component of your application using `injectIntl()`:

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { injectIntl, intlShape } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-intl'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">MyComponent</span> = (<span class="hljs-params">{ intl }</span>) => <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{`The current locale is ${intl.locale}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
<span class="hljs-title class_">MyComponent</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">intl</span>: intlShape.<span class="hljs-property">isRequired</span>,
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">injectIntl</span>(<span class="hljs-title class_">MyComponent</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
94

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#94-How-to-access-current-locale-with-react-in

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
