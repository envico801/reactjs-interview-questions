========== Question ==========  

### How do you update objects inside state?  

========== Answer ==========  

You cannot update the objects which exists in the state directly. Instead, you should create a fresh new object (or copy from the existing object) and update the latest state using the newly created object. Eventhough JavaScript objects are mutable, you need to treat objects inside state as read-only while updating the state.

Let's see this comparison with an example. The issue with regular object mutation approach can be described by updating the user details fields of `Profile` component. The properties of `Profile` component such as firstName, lastName and age details mutated in an event handler as shown below.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-keyword">import</span> { useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">Profile</span>(<span class="hljs-params"></span>) {
    <span class="hljs-keyword">const</span> [user, setUser] = <span class="hljs-title function_">useState</span>({
        <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>,
        <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Abraham'</span>,
        <span class="hljs-attr">age</span>: <span class="hljs-number">30</span>,
    });
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleFirstNameChange</span>(<span class="hljs-params">e</span>) {
        user.<span class="hljs-property">firstName</span> = e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>;
    }
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleLastNameChange</span>(<span class="hljs-params">e</span>) {
        user.<span class="hljs-property">lastName</span> = e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>;
    }
    <span class="hljs-keyword">function</span> <span class="hljs-title function_">handleAgeChange</span>(<span class="hljs-params">e</span>) {
        user.<span class="hljs-property">age</span> = e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>;
    }
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                First name:
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{user.firstName}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{handleFirstNameChange}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Last name:
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{user.lastName}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{handleLastNameChange}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">label</span>></span>
                Age:
                <span class="hljs-tag">&#x3C;<span class="hljs-name">input</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{user.age}</span> <span class="hljs-attr">onChange</span>=<span class="hljs-string">{handleAgeChange}</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">label</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">p</span>></span>
                Profile:
                {person.firstName} {person.lastName} ({person.age})
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span>
        <span class="hljs-tag">&#x3C;/></span></span>
    );
}
</code></pre>
<!-- codeblock-end -->

Once you run the application with above user profile component, you can observe that user profile details won't be update upon entering the input fields.

This issue can be fixed by creating a new copy of object which includes existing properties through spread syntax(...obj) and add changed values in a single event handler itself as shown below.

<!-- codeblock-start -->
<pre><code class="hljs language-jsx"><span class="hljs-title function_">handleProfileChange</span>(<span class="hljs-params">e</span>) {
  <span class="hljs-title function_">setUser</span>({
  ...user,
    [e.<span class="hljs-property">target</span>.<span class="hljs-property">name</span>]: e.<span class="hljs-property">target</span>.<span class="hljs-property">value</span>
  });
}
</code></pre>
<!-- codeblock-end -->

The above event handler is concise instead of maintaining separate event handler for each field. Now, UI displays the updated field values as expected without an issue.

========== Id ==========  
256

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#256-How-do-you-update-objects-inside-state

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
