========== Question ==========  

### What is the difference between HTML and React event handling?  

========== Answer ==========  

Below are some of the main differences between HTML and React event handling,

1. In HTML, the event name usually represents in _lowercase_ as a convention:

    ```html
    <button onclick="activateLasers()"></button>
    ```

    Whereas in React it follows _camelCase_ convention:

    ```jsx
    <button onClick={activateLasers}>
    ```

2. In HTML, you can return `false` to prevent default behavior:

    ```html
    <a href="#" onclick='console.log("The link was clicked."); return false;' />
    ```

    Whereas in React you must call `preventDefault()` explicitly:

    ```javascript
    function handleClick(event) {
        event.preventDefault();
        console.log('The link was clicked.');
    }
    ```

3. In HTML, you need to invoke the function by appending `()`

    Whereas in react you should not append `()` with the function name. (refer
    "activateLasers" function in the first point for example)

========== Id ==========  
12

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#12-What-is-the-difference-between-html-and-re

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
