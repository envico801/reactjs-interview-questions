========== Question ==========  

### What are the possible ways of updating objects in state?  

========== Answer ==========  

1.  **Calling `setState()` with an object to merge with state:**

    -   Using `Object.assign()` to create a copy of the object:

        ```javascript
        const user = Object.assign({}, this.state.user, { age: 42 });
        this.setState({ user });
        ```

    -   Using _spread operator_:

        ```javascript
        const user = { ...this.state.user, age: 42 };
        this.setState({ user });
        ```

2.  **Calling `setState()` with a function:**

    ```javascript
    this.setState((prevState) => ({
        user: {
            ...prevState.user,
            age: 42,
        },
    }));
    ```

========== Id ==========  
310

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#310-What-are-the-possible-ways-of-updating-obj

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
