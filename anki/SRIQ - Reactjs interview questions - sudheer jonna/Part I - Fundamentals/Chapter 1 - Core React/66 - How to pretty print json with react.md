========== Question ==========  

### How to pretty print JSON with React?  

========== Answer ==========  

We can use `<pre>` tag so that the formatting of the `JSON.stringify()` is retained:

```jsx
const data = { name: "John", age: 42 };

function User {
    return <pre>{JSON.stringify(data, null, 2)}</pre>;
}

const container = createRoot(document.getElementById("container"));

container.render(<User />);
```

  <details><summary><b>See Class</b></summary>

  <p>

```jsx
const data = { name: 'John', age: 42 };

class User extends React.Component {
    render() {
        return <pre>{JSON.stringify(data, null, 2)}</pre>;
    }
}

React.render(<User />, document.getElementById('container'));
```

  </p>

  </details>

========== Id ==========  
66

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#66-How-to-pretty-print-json-with-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
