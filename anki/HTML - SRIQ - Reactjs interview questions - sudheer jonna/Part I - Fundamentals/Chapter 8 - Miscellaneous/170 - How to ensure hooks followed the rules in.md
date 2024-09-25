========== Question ==========  

### How to ensure hooks followed the rules in your project?  

========== Answer ==========  

React team released an ESLint plugin called **eslint-plugin-react-hooks** that enforces Hook's two rules. It is part of Hooks API. You can add this plugin to your project using the below command,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">npm install eslint-plugin-react-hooks --save-dev
</code></pre>
<!-- codeblock-end -->

And apply the below config in your ESLint config file,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// Your ESLint configuration</span>
{
  <span class="hljs-string">"plugins"</span>: [
    <span class="hljs-comment">// ...</span>
    <span class="hljs-string">"react-hooks"</span>
  ],
  <span class="hljs-string">"rules"</span>: {
    <span class="hljs-comment">// ...</span>
    <span class="hljs-string">"react-hooks/rules-of-hooks"</span>: <span class="hljs-string">"error"</span>
  }
}
</code></pre>
<!-- codeblock-end -->

The recommended `eslint-config-react-app` preset already includes the hooks rules of this plugin.

For example, the linter enforce proper naming convention for hooks. If you rename your custom hooks which as prefix "use" to something else then linter won't allow you to call built-in hooks such as useState, useEffect etc inside of your custom hook anymore.

**Note:** This plugin is intended to use in Create React App by default.

========== Id ==========  
170

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#170-How-to-ensure-hooks-followed-the-rules-in

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
