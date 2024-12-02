========== Question ==========  

### How to prevent unnecessary updates using setState?  

========== Answer ==========  

You can compare the current value of the state with an existing state value and decide whether to rerender the page or not. If the values are the same then you need to return **null** to stop re-rendering otherwise return the latest state value.

For example, the user profile information is conditionally rendered as follows,

```jsx
getUserProfile = (user) => {
    const latestAddress = user.address;
    this.setState((state) => {
        if (state.address === latestAddress) {
            return null;
        } else {
            return { title: latestAddress };
        }
    });
};
```

========== Id ==========  
166

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#166-How-to-prevent-unnecessary-updates-using-s

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
