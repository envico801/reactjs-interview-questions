========== Question ==========  

### How does context works using useContext hook?  

========== Answer ==========  

The Context API in React, along with the `useContext` hook, provides a way to share data across multiple components without explicitly passing props through each level of the component tree. This is particularly useful for passing global data or for cases where many components need access to the same data.

Here's an overview of how context works with the `useContext` hook:

1. Create a context:

    First, you create a context using `React.createContext()`.

2. Provide the context:

    Wrap the parent component with a Context Provider to make the context available to all child components.

3. Consume the context:

    Use the `useContext` hook in any child component to access the context value.

Let's illustrate this with a simple example:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { createContext, useContext, useState } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-comment">// Step 1: Create a context</span>
<span class="hljs-keyword">const</span> <span class="hljs-title class_">ThemeContext</span> = <span class="hljs-title function_">createContext</span>();
<span class="hljs-comment">// Step 2: Create a provider component</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ThemeProvider</span> = (<span class="hljs-params">{ children }</span>) => {
    <span class="hljs-keyword">const</span> [theme, setTheme] = <span class="hljs-title function_">useState</span>(<span class="hljs-string">'light'</span>);
    <span class="hljs-keyword">const</span> <span class="hljs-title function_">toggleTheme</span> = (<span class="hljs-params"></span>) => {
        <span class="hljs-title function_">setTheme</span>(<span class="hljs-function">(<span class="hljs-params">prevTheme</span>) =></span> (prevTheme === <span class="hljs-string">'light'</span> ? <span class="hljs-string">'dark'</span> : <span class="hljs-string">'light'</span>));
    };
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ThemeContext.Provider</span> <span class="hljs-attr">value</span>=<span class="hljs-string">{{</span> <span class="hljs-attr">theme</span>, <span class="hljs-attr">toggleTheme</span> }}></span>{children}<span class="hljs-tag">&#x3C;/<span class="hljs-name">ThemeContext.Provider</span>></span></span>;
};
<span class="hljs-comment">// Step 3: Create components that use the context</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ThemedButton</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">const</span> { theme, toggleTheme } = <span class="hljs-title function_">useContext</span>(<span class="hljs-title class_">ThemeContext</span>);
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">button</span>
            <span class="hljs-attr">onClick</span>=<span class="hljs-string">{toggleTheme}</span>
            <span class="hljs-attr">style</span>=<span class="hljs-string">{{</span>
                <span class="hljs-attr">backgroundColor:</span> <span class="hljs-attr">theme</span> === <span class="hljs-string">'light'</span> ? '#<span class="hljs-attr">fff</span>' <span class="hljs-attr">:</span> '#<span class="hljs-attr">333</span>',
                <span class="hljs-attr">color:</span> <span class="hljs-attr">theme</span> === <span class="hljs-string">'light'</span> ? '#<span class="hljs-attr">333</span>' <span class="hljs-attr">:</span> '#<span class="hljs-attr">fff</span>',
            }}
        ></span>
            Toggle Theme
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span></span>
    );
};
<span class="hljs-keyword">const</span> <span class="hljs-title function_">ThemedText</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">const</span> { theme } = <span class="hljs-title function_">useContext</span>(<span class="hljs-title class_">ThemeContext</span>);
    <span class="hljs-keyword">return</span> <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">p</span> <span class="hljs-attr">style</span>=<span class="hljs-string">{{</span> <span class="hljs-attr">color:</span> <span class="hljs-attr">theme</span> === <span class="hljs-string">'light'</span> ? '#<span class="hljs-attr">333</span>' <span class="hljs-attr">:</span> '#<span class="hljs-attr">fff</span>' }}></span>Current theme: {theme}<span class="hljs-tag">&#x3C;/<span class="hljs-name">p</span>></span></span>;
};
<span class="hljs-comment">// Step 4: Use the provider to wrap the app</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">App</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">ThemeProvider</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">h1</span>></span>Theme Example<span class="hljs-tag">&#x3C;/<span class="hljs-name">h1</span>></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">ThemedText</span> /></span>
                <span class="hljs-tag">&#x3C;<span class="hljs-name">ThemedButton</span> /></span>
            <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">ThemeProvider</span>></span></span>
    );
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">App</span>;
</code></pre>
<!-- codeblock-end -->

Let's break down how this works:

1. We create a `ThemeContext` using `createContext()`.

2. The `ThemeProvider` component:

    - Manages the theme state.

    - Provides a function to toggle the theme.

    - Wraps its children with `ThemeContext.Provider`, passing the theme state and toggle function as the context value.

3. Child components (`ThemedButton` and `ThemedText`):

    - Use the `useContext` hook to access the theme context.

    - Can read the current theme and call the toggle function without these being passed as props.

4. The `App` component wraps everything in `ThemeProvider`, making the theme context available throughout the app.

Key benefits of using context with `useContext`:

1. Avoids prop drilling: You don't need to pass props through intermediate components.

2. Centralized state management: Useful for global states like themes, user authentication, language preferences, etc.

3. Component reusability: Components can be more easily reused as they're not tightly coupled to their data source.

4. Performance: Can potentially improve performance by reducing re-renders of intermediate components.

However, it's important to note that context should not be used for every type of state or prop. It's best suited for global or widely-used data. For local state or props that are only used by a few closely related components, regular state management or prop passing is often more appropriate.

========== Id ==========  
267

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#267-How-does-context-works-using-usecontext-ho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
