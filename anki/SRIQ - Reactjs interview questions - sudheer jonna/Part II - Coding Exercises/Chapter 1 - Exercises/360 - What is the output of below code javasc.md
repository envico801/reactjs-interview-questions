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
                    setCounter(counter + 5);
                    setCounter(counter + 5);
                    alert(counter);
                    setCounter(counter + 5);
                    setCounter(counter + 5);
                }}
            >
                Increment
            </button>
        </>
    );
}
```

-   1: Alert with 5, 5

-   2: Alert with 15, 25

-   3: Alert with 5, 10

-   4: Error: Cannot update the same state multiple times concurrently  

========== Answer ==========  

Answer: 3

State values are fixed(i.e, default value 5) in each render and setting the state only changes it for the next render. React will wait until all the code executed with in an event handler before your state updates followed by re-rendering the UI. Also, all the 3 setter function calls are replacing the calculated value. Hence, irrespective of how many times you call `setCounter(counter + 5)` the final value is 10(5+5).

This can be visuallized by substituting with state variable values in the particular render,

```javascript
<button
    onClick={() => {
        setCounter(5 + 5);
        setCounter(5 + 5);
        alert(5);
        setCounter(5 + 5);
        setCounter(5 + 5);
    }}
>
    Increment
</button>
```

========== Id ==========  
360

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part II - Coding Exercises::Chapter 1 - Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-II-Coding-Exercises::#Chapter-1-Exercises::#360-What-is-the-output-of-below-code-javasc

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
