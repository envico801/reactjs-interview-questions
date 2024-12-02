========== Question ==========  

### What are controlled components?  

========== Answer ==========  

A component that controls the input elements within the forms on subsequent user input is called **Controlled Component**, i.e, every state mutation will have an associated handler function. That means, the displayed data is always in sync with the state of the component.

The controlled components will be implemented using the below steps,

1. Initialize the state using use state hooks in function components or inside constructor for class components.

2. Set the value of the form element to the respective state variable.

3. Create an event handler to handle the user input changes through useState updater function or setState from class component.

4. Attach the above event handler to form elements change or click events

For example, the name input field updates the user name using `handleChange` event handler as below,

```javascript
import React, { useState } from 'react';

function UserProfile() {
    const [username, setUsername] = useState('');

    const handleChange = (e) => {
        setUsername(e.target.value);
    };

    return (
        <form>
            <label>
                Name:
                <input type='text' value={username} onChange={handleChange} />
            </label>
        </form>
    );
}
```

========== Id ==========  
21

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#21-What-are-controlled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
