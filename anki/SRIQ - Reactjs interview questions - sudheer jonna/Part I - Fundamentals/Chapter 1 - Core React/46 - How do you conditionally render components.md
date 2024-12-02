========== Question ==========  

### How do you conditionally render components?  

========== Answer ==========  

In some cases you want to render different components depending on some state. JSX does not render `false` or `undefined`, so you can use conditional _short-circuiting_ to render a given part of your component only if a certain condition is true.

```jsx
const MyComponent = ({ name, address }) => (
    <div>
        <h2>{name}</h2>
        {address && <p>{address}</p>}
    </div>
);
```

If you need an `if-else` condition then use _ternary operator_.

```jsx
const MyComponent = ({ name, address }) => (
    <div>
        <h2>{name}</h2>
        {address ?
            <p>{address}</p>
        :   <p>{'Address is not available'}</p>}
    </div>
);
```

========== Id ==========  
46

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#46-How-do-you-conditionally-render-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
