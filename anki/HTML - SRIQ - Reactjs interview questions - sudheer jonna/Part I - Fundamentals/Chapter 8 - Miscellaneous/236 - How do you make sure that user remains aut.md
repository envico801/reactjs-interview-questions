========== Question ==========  

### How do you make sure that user remains authenticated on page refresh while using Context API State Management?  

========== Answer ==========  

When a user logs in and reload, to persist the state generally we add the load user action in the useEffect hooks in the main App.js. While using Redux, loadUser action can be easily accessed.

**App.js**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">import</span> { loadUser } <span class="hljs-keyword">from</span> <span class="hljs-string">'../actions/auth'</span>;
store.<span class="hljs-title function_">dispatch</span>(<span class="hljs-title function_">loadUser</span>());
</code></pre>
<!-- codeblock-end -->

-   But while using **Context API**, to access context in App.js, wrap the AuthState in index.js so that App.js can access the auth context. Now whenever the page reloads, no matter what route you are on, the user will be authenticated as **loadUser** action will be triggered on each re-render.

**index.js**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">ReactDOM</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'react-dom'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">App</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./App'</span>;
<span class="hljs-keyword">import</span> <span class="hljs-title class_">AuthState</span> <span class="hljs-keyword">from</span> <span class="hljs-string">'./context/auth/AuthState'</span>;
<span class="hljs-title class_">ReactDOM</span>.<span class="hljs-title function_">render</span>(
    <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">React.StrictMode</span>></span>
        <span class="hljs-tag">&#x3C;<span class="hljs-name">AuthState</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">App</span> /></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">AuthState</span>></span>
    <span class="hljs-tag">&#x3C;/<span class="hljs-name">React.StrictMode</span>></span></span>,
    <span class="hljs-variable language_">document</span>.<span class="hljs-title function_">getElementById</span>(<span class="hljs-string">'root'</span>),
);
</code></pre>
<!-- codeblock-end -->

**App.js**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> authContext = <span class="hljs-title function_">useContext</span>(<span class="hljs-title class_">AuthContext</span>);
<span class="hljs-keyword">const</span> { loadUser } = authContext;
<span class="hljs-title function_">useEffect</span>(<span class="hljs-function">() =></span> {
    <span class="hljs-title function_">loadUser</span>();
}, []);
</code></pre>
<!-- codeblock-end -->

**loadUser**

<!-- codeblock-start -->
<pre><code class="hljs language-js"><span class="hljs-keyword">const</span> <span class="hljs-title function_">loadUser</span> = <span class="hljs-keyword">async</span> (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">const</span> token = <span class="hljs-variable language_">sessionStorage</span>.<span class="hljs-title function_">getItem</span>(<span class="hljs-string">'token'</span>);
    <span class="hljs-keyword">if</span> (!token) {
        <span class="hljs-title function_">dispatch</span>({
            <span class="hljs-attr">type</span>: <span class="hljs-variable constant_">ERROR</span>,
        });
    }
    <span class="hljs-title function_">setAuthToken</span>(token);
    <span class="hljs-keyword">try</span> {
        <span class="hljs-keyword">const</span> res = <span class="hljs-keyword">await</span> <span class="hljs-title function_">axios</span>(<span class="hljs-string">'/api/auth'</span>);
        <span class="hljs-title function_">dispatch</span>({
            <span class="hljs-attr">type</span>: <span class="hljs-variable constant_">USER_LOADED</span>,
            <span class="hljs-attr">payload</span>: res.<span class="hljs-property">data</span>.<span class="hljs-property">data</span>,
        });
    } <span class="hljs-keyword">catch</span> (err) {
        <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">error</span>(err);
    }
};
</code></pre>
<!-- codeblock-end -->

========== Id ==========  
236

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#236-How-do-you-make-sure-that-user-remains-aut

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
