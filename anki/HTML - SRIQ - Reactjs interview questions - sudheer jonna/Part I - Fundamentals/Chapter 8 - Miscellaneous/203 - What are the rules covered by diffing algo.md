========== Question ==========  

### What are the rules covered by diffing algorithm?  

========== Answer ==========  

When diffing two trees, React first compares the two root elements. The behavior is different depending on the types of the root elements. It covers the below rules during reconciliation algorithm,

1.  **Elements Of Different Types:**

    Whenever the root elements have different types, React will tear down the old tree and build the new tree from scratch. For example, elements `<a>` to `<img>`, or from `<Article>` to `<Comment>` of different types lead a full rebuild.

2.  **DOM Elements Of The Same Type:**

    When comparing two React DOM elements of the same type, React looks at the attributes of both, keeps the same underlying DOM node, and only updates the changed attributes. Lets take an example with same DOM elements except className attribute,

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        &#x3C;div className=<span class="hljs-string">"show"</span> title=<span class="hljs-string">"ReactJS"</span> />
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span> <span class="hljs-attr">className</span>=<span class="hljs-string">"hide"</span> <span class="hljs-attr">title</span>=<span class="hljs-string">"ReactJS"</span> /></span></span>
        </code></pre>
    <!-- codeblock-end -->

3.  **Component Elements Of The Same Type:**

    When a component updates, the instance stays the same, so that state is maintained across renders. React updates the props of the underlying component instance to match the new element, and calls componentWillReceiveProps() and componentWillUpdate() on the underlying instance. After that, the render() method is called and the diff algorithm recurses on the previous result and the new result.

4.  **Recursing On Children:**

    when recursing on the children of a DOM node, React just iterates over both lists of children at the same time and generates a mutation whenever there’s a difference. For example, when adding an element at the end of the children, converting between these two trees works well.

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        &#x3C;ul>
          <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>first<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>
          <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>second<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>
        &#x3C;/ul>
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
          <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>first<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
          <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>second<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
          <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span>></span>third<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
        </code></pre>
    <!-- codeblock-end -->

5.  **Handling keys:**

    React supports a key attribute. When children have keys, React uses the key to match children in the original tree with children in the subsequent tree. For example, adding a key can make the tree conversion efficient,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">&#x3C;ul>
  <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">"2015"</span>></span>Duke<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>
  <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">"2016"</span>></span>Villanova<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span></span>
&#x3C;/ul>
<span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">"2014"</span>></span>Connecticut<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">"2015"</span>></span>Duke<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
  <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">"2016"</span>></span>Villanova<span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
<span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
203

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#203-What-are-the-rules-covered-by-diffing-algo

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store