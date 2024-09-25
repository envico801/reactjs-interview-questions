========== Question ==========  

### What is JSX?  

========== Answer ==========  

_JSX_ stands for _JavaScript XML_ and it is an XML-like syntax extension to
ECMAScript. Basically it just provides the syntactic sugar for the
`React.createElement(type, props, ...children)` function, giving us
expressiveness of JavaScript along with HTML like template syntax.

In the example below, the text inside `<h1>` tag is returned as JavaScript
function to the render function.

```jsx
export default function App() {
    return <h1 className='greeting'>{'Hello, this is a JSX Code!'}</h1>;
}
```

If you don't use JSX syntax then the respective JavaScript code should be
written as below,

```javascript
import { createElement } from 'react';
export default function App() {
    return createElement(
        'h1',
        { className: 'greeting' },
        'Hello, this is a JSX Code!',
    );
}
```

 <details><summary><b>See Class</b></summary>

 <p>

```jsx
class App extends React.Component {
    render() {
        return <h1 className='greeting'>{'Hello, this is a JSX Code!'}</h1>;
    }
}
```

 </p>

 </details>

**Note:** JSX is stricter than HTML

========== Id ==========  
4

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#4-What-is-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
