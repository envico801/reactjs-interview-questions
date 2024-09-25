========== Question ==========  

### How do you say that state updates are merged?  

========== Answer ==========  

When you call setState() in the component, React merges the object you provide into the current state.

For example, let us take a facebook user with posts and comments details as state variables,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript">  <span class="hljs-title function_">constructor</span>(<span class="hljs-params">props</span>) {
    <span class="hljs-variable language_">super</span>(props);
    <span class="hljs-variable language_">this</span>.<span class="hljs-property">state</span> = {
      <span class="hljs-attr">posts</span>: [],
      <span class="hljs-attr">comments</span>: []
    };
  }
</code></pre>
<!-- codeblock-end -->

Now you can update them independently with separate `setState()` calls as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"> <span class="hljs-title function_">componentDidMount</span>(<span class="hljs-params"></span>) {
    <span class="hljs-title function_">fetchPosts</span>().<span class="hljs-title function_">then</span>(<span class="hljs-function"><span class="hljs-params">response</span> =></span> {
      <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
        <span class="hljs-attr">posts</span>: response.<span class="hljs-property">posts</span>
      });
    });
    <span class="hljs-title function_">fetchComments</span>().<span class="hljs-title function_">then</span>(<span class="hljs-function"><span class="hljs-params">response</span> =></span> {
      <span class="hljs-variable language_">this</span>.<span class="hljs-title function_">setState</span>({
        <span class="hljs-attr">comments</span>: response.<span class="hljs-property">comments</span>
      });
    });
  }
</code></pre>
<!-- codeblock-end -->

As mentioned in the above code snippets, `this.setState({comments})` updates only comments variable without modifying or replacing `posts` variable.

========== Id ==========  
342

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#342-How-do-you-say-that-state-updates-are-merg

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
