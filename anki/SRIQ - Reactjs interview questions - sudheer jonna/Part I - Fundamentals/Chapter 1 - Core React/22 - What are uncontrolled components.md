========== Question ==========  

### What are uncontrolled components?  

========== Answer ==========  

The **Uncontrolled Components** are the ones that store their own state internally, and you query the DOM using a ref to find its current value when you need it. This is a bit more like traditional HTML.

The uncontrolled components will be implemented using the below steps,

1. Create a ref using useRef react hook in function component or `React.createRef()` in class based component.

2. Attach this ref to the form element.

3. The form element value can be accessed directly through `ref` in event handlers or `componentDidMount` for class components

In the below UserProfile component, the `username` input is accessed using ref.

```jsx
import React, { useRef } from 'react';
function UserProfile() {
    const usernameRef = useRef(null);
    const handleSubmit = (event) => {
        event.preventDefault();
        console.log('The submitted username is: ' + usernameRef.current.value);
    };
    return (
        <form onSubmit={handleSubmit}>
            <label>
                Username:
                <input type='text' ref={usernameRef} />
            </label>
            <button type='submit'>Submit</button>
        </form>
    );
}
```

In most cases, it's recommend to use controlled components to implement forms. In a controlled component, form data is handled by a React component. The alternative is uncontrolled components, where form data is handled by the DOM itself.

<details><summary><b>See Class</b></summary>

<p>

```jsx
class UserProfile extends React.Component {
    constructor(props) {
        super(props);
        this.handleSubmit = this.handleSubmit.bind(this);
        this.input = React.createRef();
    }
    handleSubmit(event) {
        alert('A name was submitted: ' + this.input.current.value);
        event.preventDefault();
    }
    render() {
        return (
            <form onSubmit={this.handleSubmit}>
                <label>
                    {'Name:'}
                    <input type='text' ref={this.input} />
                </label>
                <input type='submit' value='Submit' />
            </form>
        );
    }
}
```

</p>

</details>

========== Id ==========  
22

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#22-What-are-uncontrolled-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
