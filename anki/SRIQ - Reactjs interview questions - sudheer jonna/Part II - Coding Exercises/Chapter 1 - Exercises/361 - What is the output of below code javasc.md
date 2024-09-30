========== Question ==========  

### What is the output of below code

```javascript
import { useState } from 'react';
export default function Counter() {
    const [counter, setCounter] = useState(5);
    return (
        <>
            <span>{counter}</span>
            <button
                onClick={() => {
                    setCounter((counter) => counter + 5);
                    setCounter((counter) => counter + 5);
                    alert(counter);
                    setCounter((counter) => counter + 5);
                    setCounter((counter) => counter + 5);
                }}
            >
                Increment
            </button>
        </>
    );
}
```

-   1: Alert with 5, 25

-   2: Alert with 5, 10

-   3: Alert with 15, 25

-   4: Alert with 15, 10  

========== Answer ==========  

Answer: 1

React queues all the updater functions(e.g, counter => counter + 5) which will be processed after all the code inside event handler has been executed. During the next re-render(state update through setState), React goes through the queue and increment the counter based on the previous value in each function call. So the final value of counter becomes 25(initial value 5 + 5 + 5 + 5 + 5) whereas the alert shows default value 5 because the counter value won't be updated by that time.

========== Id ==========  
361

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part II - Coding Exercises::Chapter 1 - Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-II-Coding-Exercises::#Chapter-1-Exercises::#361-What-is-the-output-of-below-code-javasc

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
