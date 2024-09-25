========== Question ==========  

### What is state in React?  

========== Answer ==========  

_State_ of a component is an object that holds some information that may change
over the lifetime of the component. The important point is whenever the state
object changes, the component re-renders. It is always recommended to make our
state as simple as possible and minimize the number of stateful components.

![state](../../../../images/state.jpg)

Let's take an example of **User** component with `message` state. Here,
**useState** hook has been used to add state to the User component and it
returns an array with current state and function to update it.

```jsx
import { useState } from 'react';
function User() {
    const [message, setMessage] = useState('Welcome to React world');
    return (
        <div>
            <h1>{message}</h1>
        </div>
    );
}
```

Whenever React calls your component or access `useState` hook, it gives you a
snapshot of the state for that particular render.

<details><summary><b>See Class</b></summary>

<p>

```jsx
import React from 'react';
class User extends React.Component {
    constructor(props) {
        super(props);
        this.state = {
            message: 'Welcome to React world',
        };
    }
    render() {
        return (
            <div>
                <h1>{this.state.message}</h1>
            </div>
        );
    }
}
```

</p>

</details>

State is similar to props, but it is private and fully controlled by the
component ,i.e., it is not accessible to any other component till the owner
component decides to pass it.

========== Id ==========  
9

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#9-What-is-state-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
