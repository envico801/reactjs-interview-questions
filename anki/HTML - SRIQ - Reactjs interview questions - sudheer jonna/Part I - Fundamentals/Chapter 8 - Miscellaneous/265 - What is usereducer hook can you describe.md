========== Question ==========  

### What is useReducer hook? Can you describe its usage?  

========== Answer ==========  

The `useReducer` hook is a React hook that provides an alternative to `useState` for managing complex state logic in functional components. It's particularly useful when you have state transitions that depend on the previous state or when the next state is determined by multiple sub-values.

Here's a brief overview of `useReducer`:

1. Basic structure:

    <!-- codeblock-start -->
    <pre><code class="hljs language-javascript">
        <span class="hljs-keyword">const</span> [state, dispatch] = <span class="hljs-title function_">useReducer</span>(reducer, initialState);
        </code></pre>
    <!-- codeblock-end -->

2. Components:

    - `state`: The current state value

    - `dispatch`: A function to send actions to update the state

    - `reducer`: A pure function that takes the current state and an action, and returns the new state

    - `initialState`: The initial state value

3. Usage:

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">import</span> <span class="hljs-title class_">React</span>, { useReducer } <span class="hljs-keyword">from</span> <span class="hljs-string">'react'</span>;
<span class="hljs-comment">// Reducer function</span>
<span class="hljs-keyword">const</span> <span class="hljs-title function_">counterReducer</span> = (<span class="hljs-params">state, action</span>) => {
    <span class="hljs-keyword">switch</span> (action.<span class="hljs-property">type</span>) {
        <span class="hljs-keyword">case</span> <span class="hljs-string">'INCREMENT'</span>:
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">count</span>: state.<span class="hljs-property">count</span> + <span class="hljs-number">1</span> };
        <span class="hljs-keyword">case</span> <span class="hljs-string">'DECREMENT'</span>:
            <span class="hljs-keyword">return</span> { <span class="hljs-attr">count</span>: state.<span class="hljs-property">count</span> - <span class="hljs-number">1</span> };
        <span class="hljs-attr">default</span>:
            <span class="hljs-keyword">return</span> state;
    }
};
<span class="hljs-keyword">const</span> <span class="hljs-title function_">Counter</span> = (<span class="hljs-params"></span>) => {
    <span class="hljs-comment">// Using useReducer</span>
    <span class="hljs-keyword">const</span> [state, dispatch] = <span class="hljs-title function_">useReducer</span>(counterReducer, { <span class="hljs-attr">count</span>: <span class="hljs-number">0</span> });
    <span class="hljs-keyword">return</span> (
        <span class="xml"><span class="hljs-tag">&#x3C;<span class="hljs-name">div</span>></span>
            Count: {state.count}
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> dispatch({ type: 'INCREMENT' })}>+<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
            <span class="hljs-tag">&#x3C;<span class="hljs-name">button</span> <span class="hljs-attr">onClick</span>=<span class="hljs-string">{()</span> =></span> dispatch({ type: 'DECREMENT' })}>-<span class="hljs-tag">&#x3C;/<span class="hljs-name">button</span>></span>
        <span class="hljs-tag">&#x3C;/<span class="hljs-name">div</span>></span></span>
    );
};
<span class="hljs-keyword">export</span> <span class="hljs-keyword">default</span> <span class="hljs-title class_">Counter</span>;
</code></pre>
<!-- codeblock-end -->

In this example:

1. We define a `counterReducer` function that specifies how the state should change in response to different actions.

2. The `useReducer` hook is called with the reducer function and an initial state.

3. We use the `dispatch` function to send actions to the reducer, which then updates the state.

4. The component re-renders with the new state when an action is dispatched.

Key benefits of `useReducer`:

1. Centralized state logic: All state update logic is contained in the reducer function.

2. Predictable state changes: The reducer must return a new state for any given current state and action.

3. Easier testing: Reducer functions are pure and can be easily unit tested.

4. Complex state transitions: Useful for managing state that involves multiple sub-values or when the next state depends on the previous one.

5. Performance optimization: Can be more efficient than `useState` for complex state logic.

========== Id ==========  
265

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#265-What-is-usereducer-hook-can-you-describe

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
