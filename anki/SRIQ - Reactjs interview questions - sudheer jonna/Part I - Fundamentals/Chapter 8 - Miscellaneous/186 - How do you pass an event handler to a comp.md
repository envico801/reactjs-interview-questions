========== Question ==========  

### How do you pass an event handler to a component?  

========== Answer ==========  

You can pass event handlers and other functions as props to child components. The functions can be passed to child component as below,

```jsx
function Button({ onClick }) {
    return <button onClick={onClick}>Download</button>;
}

export default function downloadExcel() {
    function handleClick() {
        alert('Downloaded');
    }

    return <Button onClick={handleClick}></Button>;
}
```

========== Id ==========  
186

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#186-How-do-you-pass-an-event-handler-to-a-comp

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
