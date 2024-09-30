========== Question ==========  

### How to pass numbers to React component?  

========== Answer ==========  

We can pass `numbers` as `props` to React component using curly braces `{}` where as `strings` in double quotes `""` or single quotes `''`

```jsx
import React from 'react';
const ChildComponent = ({ name, age }) => {
    return (
        <>
            My Name is {name} and Age is {age}
        </>
    );
};
const ParentComponent = () => {
    return (
        <>
            <ChildComponent name='Chetan' age={30} />
        </>
    );
};
export default ParentComponent;
```

========== Id ==========  
161

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#161-How-to-pass-numbers-to-react-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
