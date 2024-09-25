========== Question ==========  

### What are stateful components?  

========== Answer ==========  

If the behaviour of a component is dependent on the _state_ of the component
then it can be termed as stateful component. These _stateful components_ are
either function components with hooks or _class components_.

Let's take an example of function stateful component which update the state
based on click event,

```javascript
import React, {useState} from 'react';
const App = (props) => {
const [count, setCount] = useState(0);
handleIncrement() {
  setCount(count+1);
}
return (
  <>
    <button onClick={handleIncrement}>Increment</button>
    <span>Counter: {count}</span>
  </>
  )
}
```

<details><summary><b>See Class</b></summary>

<p>

The equivalent class stateful component with a state that gets initialized in
the `constructor`.

```jsx
class App extends Component {
    constructor(props) {
        super(props);
        this.state = { count: 0 };
    }
    handleIncrement() {
        setState({ count: this.state.count + 1 });
    }
    render() {
        <>
            <button onClick={() => this.handleIncrement}>Increment</button>
            <span>Count: {count}</span>
        </>;
    }
}
```

</p>

</details>

========== Id ==========  
35

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#35-What-are-stateful-components

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
