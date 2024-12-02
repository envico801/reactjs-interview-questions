========== Question ==========  

### How does React batch multiple state updates?  

========== Answer ==========  

React prevents component from re-rendering for each and every state update by grouping multiple state updates within an event handler. This strategy improves the application performance and this process known as **batching**. The older version of React only supported batching for browser events whereas React18 supported for asynchronous actions, timeouts and intervals along with native events. This improved version of batching is called **automatic batching**.

Let's demonstrate this automatic batching feature with a below example.

```jsx
import { useState } from 'react';

export default function BatchingState() {
    const [count, setCount] = useState(0);
    const [message, setMessage] = useState('batching');

    console.log('Application Rendered');

    const handleUsers = () => {
        fetch('https://jsonplaceholder.typicode.com/users/1').then(() => {
            // Automatic Batching re-render only once
            setCount(count + 1);
            setMessage('users fetched');
        });
    };

    return (
        <>
            <h1>{count}</h1>
            <button onClick={handleAsyncFetch}>Click Me!</button>
        </>
    );
}
```

The preceding code updated two state variables with in an event handler. However, React will perform automatic batching feature and the component will be re-rendered only once for better performance.

========== Id ==========  
253

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#253-How-does-react-batch-multiple-state-update

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
