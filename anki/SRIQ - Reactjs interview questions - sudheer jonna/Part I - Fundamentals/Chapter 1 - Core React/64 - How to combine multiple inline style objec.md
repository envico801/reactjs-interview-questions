========== Question ==========  

### How to combine multiple inline style objects?  

========== Answer ==========  

You can use _spread operator_ in regular React:

```jsx
<button style={{ ...styles.panel.button, ...styles.panel.submitButton }}>
    {'Submit'}
</button>
```

If you're using React Native then you can use the array notation:

```jsx
<button style={[styles.panel.button, styles.panel.submitButton]}>
    {'Submit'}
</button>
```

========== Id ==========  
64

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#64-How-to-combine-multiple-inline-style-objec

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
