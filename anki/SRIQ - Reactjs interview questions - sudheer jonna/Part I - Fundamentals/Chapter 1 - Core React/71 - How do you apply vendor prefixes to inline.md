========== Question ==========  

### How do you apply vendor prefixes to inline styles in React?  

========== Answer ==========  

React _does not_ apply _vendor prefixes_ automatically. You need to add vendor prefixes manually.

```jsx
<div
    style={{
        transform: 'rotate(90deg)',
        WebkitTransform: 'rotate(90deg)', // note the capital 'W' here
        msTransform: 'rotate(90deg)', // 'ms' is the only lowercase vendor prefix
    }}
/>
```

========== Id ==========  
71

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#71-How-do-you-apply-vendor-prefixes-to-inline

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
