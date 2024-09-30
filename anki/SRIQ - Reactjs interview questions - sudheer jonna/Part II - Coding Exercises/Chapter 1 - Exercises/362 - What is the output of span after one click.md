========== Question ==========  

### What is the output of span after one click?

```javascript
import { useRef } from 'react';
export default function Counter() {
    let countRef = useRef(0);
    function handleIncrement() {
        countRef.current = countRef.current + 1;
    }
    return;
    <>
        <span>Count: {countRef.current}</span>
        <button onClick={handleIncrement}>Click me</button>
    </>;
}
```

-   1: Cannot read current property of undefined

-   2: Count: 1

-   3: null

-   4: Count: 0  

========== Answer ==========  

Answer: 4

In React, every update has two phases.

1. **Render:** This is where React calls the components in order to output something on the screen

2. **Commit:** React applies changes to the DOM

Any updates to the ref will be reflected only in the commit phase. In other words, React sets **counterRef.current** during the commit phase. Hence, **countRef.current** always holds value `0` irrespective of how many times the Increment button clicked.

========== Id ==========  
362

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part II - Coding Exercises::Chapter 1 - Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-II-Coding-Exercises::#Chapter-1-Exercises::#362-What-is-the-output-of-span-after-one-click

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
