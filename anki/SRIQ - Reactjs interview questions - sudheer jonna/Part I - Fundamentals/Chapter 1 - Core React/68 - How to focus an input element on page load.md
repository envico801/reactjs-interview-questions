========== Question ==========  

### How to focus an input element on page load?  

========== Answer ==========  

You need to use `useEffect` hook to set focus on input field during page load
time for functional component.

```jsx
import React, { useEffect, useRef } from 'react';
const App = () => {
    const inputElRef = useRef(null);
    useEffect(() => {
        inputElRef.current.focus();
    }, []);
    return (
        <div>
            <input defaultValue={"Won't focus"} />
            <input ref={inputElRef} defaultValue={'Will focus'} />
        </div>
    );
};
ReactDOM.render(<App />, document.getElementById('app'));
```

  <details><summary><b>See Class</b></summary>

  <p>

You can do it by creating _ref_ for `input` element and using it in
`componentDidMount()`:

```jsx
class App extends React.Component {
    componentDidMount() {
        this.nameInput.focus();
    }
    render() {
        return (
            <div>
                <input defaultValue={"Won't focus"} />
                <input
                    ref={(input) => (this.nameInput = input)}
                    defaultValue={'Will focus'}
                />
            </div>
        );
    }
}
ReactDOM.render(<App />, document.getElementById('app'));
```

  </p>

  </details>

========== Id ==========  
68

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#68-How-to-focus-an-input-element-on-page-load

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
