========== Question ==========  

### How to use Polymer in React?  

========== Answer ==========  

You need to follow below steps to use Polymer in React,

1.  Create a Polymer element:

    <!-- codeblock-start -->
    <pre><code class="hljs language-jsx">
        &#x3C;link rel=<span class="hljs-string">'import'</span> href=<span class="hljs-string">'../../bower_components/polymer/polymer.html'</span> />;
        <span class="hljs-title class_">Polymer</span>({
            <span class="hljs-attr">is</span>: <span class="hljs-string">'calendar-element'</span>,
            <span class="hljs-attr">ready</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
                <span class="hljs-variable language_">this</span>.<span class="hljs-property">textContent</span> = <span class="hljs-string">'I am a calendar'</span>;
            },
        });
        </code></pre>
    <!-- codeblock-end -->

2.  Create the Polymer component HTML tag by importing it in a HTML document, e.g. import it in the `index.html` of your React application:

    <!-- codeblock-start -->
    <pre><code class="hljs language-html">
        <span class="hljs-tag">&#x3C;<span class="hljs-name">link</span> <span class="hljs-attr">rel</span>=<span class="hljs-string">"import"</span> <span class="hljs-attr">href</span>=<span class="hljs-string">"./src/polymer-components/calendar-element.html"</span> /></span>
        </code></pre>
    <!-- codeblock-end -->

3.  Use that element in the JSX file:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title class_">MyComponent</span> {
          <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">calendar-element</span> /></span></span>;
        }
        </code></pre>
    <!-- codeblock-end -->

========== Id ==========  
146

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 7 - React supported libraries Integration

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-7-React-supported-libraries-Integration::#146-How-to-use-polymer-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
