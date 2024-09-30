========== Question ==========  

### How to import and export components using React and ES6?  

========== Answer ==========  

You should use default for exporting the components

```jsx
import User from "user";
export default function MyProfile {
    return <User type="customer">//...</User>;
}
```

<details><summary><b>See Class</b></summary>

<p>

```jsx
import React from 'react';
import User from 'user';
export default class MyProfile extends React.Component {
    render() {
        return <User type='customer'>//...</User>;
    }
}
```

</p>

</details>

With the export specifier, the MyProfile is going to be the member and exported to this module and the same can be imported without mentioning the name in other components.

========== Id ==========  
72

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#72-How-to-import-and-export-components-using

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
