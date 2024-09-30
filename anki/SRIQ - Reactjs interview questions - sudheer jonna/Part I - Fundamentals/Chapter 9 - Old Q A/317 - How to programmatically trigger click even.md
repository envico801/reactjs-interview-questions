========== Question ==========  

### How to programmatically trigger click event in React?  

========== Answer ==========  

You could use the ref prop to acquire a reference to the underlying `HTMLInputElement` object through a callback, store the reference as a class property, then use that reference to later trigger a click from your event handlers using the `HTMLElement.click` method.

This can be done in two steps:

1.  Create ref in render method:

    ```jsx
    <input ref={(input) => (this.inputElement = input)} />
    ```

2.  Apply click event in your event handler:

    ```javascript
    this.inputElement.click();
    ```

========== Id ==========  
317

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#317-How-to-programmatically-trigger-click-even

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
