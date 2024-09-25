========== Question ==========  

### How to format date using React Intl?  

========== Answer ==========  

The `injectIntl()` higher-order component will give you access to the `formatDate()` method via the props in your component. The method is used internally by instances of `FormattedDate` and it returns the string representation of the formatted date.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { injectIntl, intlShape } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-intl'</span>;
<span class="hljs-keyword">const</span> stringDate = <span class="hljs-variable language_">this</span>.<span class="hljs-property">props</span>.<span class="hljs-property">intl</span>.<span class="hljs-title function_">formatDate</span>(date, {
    <span class="hljs-attr">year</span>: <span class="hljs-string">'numeric'</span>,
    <span class="hljs-attr">month</span>: <span class="hljs-string">'numeric'</span>,
    <span class="hljs-attr">day</span>: <span class="hljs-string">'numeric'</span>,
});
<span class="hljs-keyword">const</span> <span class="hljs-title function_">MyComponent</span> = (<span class="hljs-params">{ intl }</span>) => <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>{`The formatted date is ${stringDate}`}<span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>;
<span class="hljs-title class_">MyComponent</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">intl</span>: intlShape.<span class="hljs-property">isRequired</span>,
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">injectIntl</span>(<span class="hljs-title class_">MyComponent</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
95

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#95-How-to-format-date-using-react-intl

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
