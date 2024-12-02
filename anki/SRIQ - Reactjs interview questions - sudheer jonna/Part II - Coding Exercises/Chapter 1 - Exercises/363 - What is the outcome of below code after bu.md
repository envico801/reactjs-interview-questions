========== Question ==========  

### What is the outcome of below code after button click?

```javascript
import { useRef } from 'react';

function MyCustomInput(props) {
    return <input {...props} />;
}

export default function MyCustomForm() {
    const inputRef = useRef(null);

    function handleInputFocus() {
        inputRef.current.focus();
    }

    return (
        <>
            <MyCustomInput ref={inputRef} />
            <button onClick={handleInputFocus}>Click Me</button>
        </>
    );
}
```

-   1: Input gets the focus

-   2: Warning: Function components cannot be given refs.

-   3: Cannot read current property of undefined

-   4: Warning: Missing ref on `<input />` element  

========== Answer ==========  

Answer: 2

By default, React does not allow a component access the DOM nodes of other components even for child components. If you still try to access the DOM nodes directly then you will receive below error:

```javascript
Warning: Function components cannot be given refs. Attempts to access this ref will fail. Did you mean to use React.forwardRef()?
```

This issue can be fixed by wrapping the **`<MyCustomInput />`** component with `forwardRef` function which accepts ref as the second argument which can be used on the **`<input />`** element as **ref={ref}**

========== Id ==========  
363

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part II - Coding Exercises::Chapter 1 - Exercises

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-II-Coding-Exercises::#Chapter-1-Exercises::#363-What-is-the-outcome-of-below-code-after-bu

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
