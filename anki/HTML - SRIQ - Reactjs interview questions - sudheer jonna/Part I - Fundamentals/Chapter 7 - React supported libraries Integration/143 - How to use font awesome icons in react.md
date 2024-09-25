========== Question ==========  

### How to use Font Awesome icons in React?  

========== Answer ==========  

The below steps followed to include Font Awesome in React:

1.  Install `font-awesome`:

    <!-- codeblock-start -->
    <pre><code class="hljs language-console">        $ npm install --save font-awesome
        </code></pre>
    <!-- codeblock-end -->

2.  Import `font-awesome` in your `index.js` file:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">import</span> <span class="hljs-string">'font-awesome/css/font-awesome.min.css'</span>;
        </code></pre>
    <!-- codeblock-end -->

3.  Add Font Awesome classes in `className`:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">function</span> <span class="hljs-title class_">MyComponent</span> {
          <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span><span class="hljs-tag">&#x3C;<span class="hljs-name">i</span> <span class="hljs-attr">className</span>=<span class="hljs-string">{</span>'<span class="hljs-attr">fa</span> <span class="hljs-attr">fa-spinner</span>'} /></span><span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
        }
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
143

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#143-How-to-use-font-awesome-icons-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
