========== Question ==========  

### Why does strict mode render twice in React?  

========== Answer ==========  

StrictMode renders components twice in development mode(not production) in order to detect any problems with your code and warn you about those problems. This is used to detect accidental side effects in the render phase. If you used `create-react-app` development tool then it automatically enables StrictMode by default.

```js
const root = createRoot(document.getElementById('root'));
root.render(
    <StrictMode>
        <App />
    </StrictMode>,
);
```

If you want to disable this behavior then you can simply remove `strict` mode.

```js
const root = createRoot(document.getElementById('root'));
root.render(<App />);
```

To detect side effects the following functions are invoked twice:

1.  Function component bodies, excluding the code inside event handlers.

2.  Functions passed to `useState`, `useMemo`, or `useReducer` (any other Hook)

3.  Class component's `constructor`, `render`, and `shouldComponentUpdate` methods

4.  Class component static `getDerivedStateFromProps` method

5.  State updater functions

========== Id ==========  
247

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#247-Why-does-strict-mode-render-twice-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
