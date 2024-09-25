========== Question ==========  

### How to fetch data with React Hooks?  

========== Answer ==========  

The effect hook called `useEffect` can be used to fetch data from an API and to set the data in the local state of the component with the useState hook’s update function.

Here is an example of fetching a list of react articles from an API using fetch.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">App</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [data, setData] = <span class="hljs-title class_">React</span>.<span class="hljs-title function_">useState</span>({ <span class="hljs-attr">hits</span>: [] });
    <span class="hljs-title class_">React</span>.<span class="hljs-title function_">useEffect</span>(<span class="hljs-function">() =></span> {
        <span class="hljs-title function_">fetch</span>(<span class="hljs-string">'http://hn.algolia.com/api/v1/search?query=react'</span>)
            .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">response</span>) =></span> response.<span class="hljs-title function_">json</span>())
            .<span class="hljs-title function_">then</span>(<span class="hljs-function">(<span class="hljs-params">data</span>) =></span> <span class="hljs-title function_">setData</span>(data));
    }, []);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ul</span>></span>
            {data.hits.map((item) => (
                <span class="hljs-tag">&#x3C;<span class="hljs-name">li</span> <span class="hljs-attr">key</span>=<span class="hljs-string">{item.objectID}</span>></span>
                    <span class="hljs-tag">&#x3C;<span class="hljs-name">a</span> <span class="hljs-attr">href</span>=<span class="hljs-string">{item.url}</span>></span>{item.title}<span class="hljs-tag">&#x3C;/<span class="hljs-name">a</span>></span>
                <span class="hljs-tag">&#x3C;/<span class="hljs-name">li</span>></span>
            ))}
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">ul</span>></span></span>
    );
}
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">App</span>;
</code></pre>
<!-- codeblock-end -->

A popular way to simplify this is by using the library axios.

We provided an empty array as second argument to the useEffect hook to avoid activating it on component updates. This way, it only fetches on component mount.

========== Id ==========  
217

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#217-How-to-fetch-data-with-react-hooks

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
