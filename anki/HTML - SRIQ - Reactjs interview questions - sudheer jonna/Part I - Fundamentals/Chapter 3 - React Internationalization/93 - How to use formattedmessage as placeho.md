========== Question ==========  

### How to use `<FormattedMessage>` as placeholder using React Intl?  

========== Answer ==========  

The `<Formatted... />` components from `react-intl` return elements, not plain text, so they can't be used for placeholders, alt text, etc. In that case, you should use lower level API `formatMessage()`. You can inject the `intl` object into your component using `injectIntl()` higher-order component and then format the message using `formatMessage()` available on that object.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> { injectIntl, intlShape } <span class="hljs-keyword">from</span> <span class="hljs-string">'react-intl'</span>;
<span class="hljs-keyword">const</span> <span class="hljs-title function_">MyComponent</span> = (<span class="hljs-params">{ intl }</span>) => {
    <span class="hljs-keyword">const</span> placeholder = intl.<span class="hljs-title function_">formatMessage</span>({ <span class="hljs-attr">id</span>: <span class="hljs-string">'messageId'</span> });
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">placeholder</span>=<span class="hljs-string">{placeholder}</span> /></span></span>;
};
<span class="hljs-title class_">MyComponent</span>.<span class="hljs-property">propTypes</span> = {
    <span class="hljs-attr">intl</span>: intlShape.<span class="hljs-property">isRequired</span>,
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title function_">injectIntl</span>(<span class="hljs-title class_">MyComponent</span>);
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
93

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#93-How-to-use-formattedmessage-as-placeho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
