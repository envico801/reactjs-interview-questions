========== Question ==========  

### What is the outcome of number of clicks after 3 button clicks?

```javascript
import { useRef } from 'react';
export default function Counter() {
    let ref = useRef(0);
    function handleClick() {
        ref.current = ref.current + 1;
    }
    return (
        <>
            <div>Clicked + {ref.current} + times</div>
            <button onClick={handleClick}>Click me!</button>
        </>
    );
}
```

-   1: 3 times

-   2: 4 times

-   3: 2 times

-   4: 0 times  

========== Answer ==========  

Answer: 4

If you try to use **{ref.current}** in the render method, the number won’t be updated on click. This is because **ref.current** does not trigger a re-render unlike state. This property is mainly used to read and write the values inside event handler or outside the render method.

========== Id ==========  
364

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part II - Coding Exercises::Chapter 1 - Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-II-Coding-Exercises::#Chapter-1-Exercises::#364-What-is-the-outcome-of-number-of-clicks-af

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
