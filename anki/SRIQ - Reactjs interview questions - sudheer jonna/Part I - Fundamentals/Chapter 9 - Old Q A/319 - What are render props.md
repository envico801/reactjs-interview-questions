========== Question ==========  

### What are render props?  

========== Answer ==========  

**Render Props** is a simple technique for sharing code between components using
a prop whose value is a function. The below component uses render prop which
returns a React element.

```jsx
<DataProvider render={(data) => <h1>{`Hello ${data.target}`}</h1>} />
```

Libraries such as React Router and DownShift are using this pattern.

========== Id ==========  
319

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#319-What-are-render-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
