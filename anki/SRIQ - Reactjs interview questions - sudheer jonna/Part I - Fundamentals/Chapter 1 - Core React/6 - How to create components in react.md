========== Question ==========  

### How to create components in React?  

========== Answer ==========  

Components are the building blocks of creating User Interfaces(UI) in React. There are two possible ways to create a component.

1. **Function Components:** This is the simplest way to create a component. Those are pure JavaScript functions that accept props object as the one and only one parameter and return React elements to render the output:

    ```jsx
    function Greeting({ message }) {
        return <h1>{`Hello, ${message}`}</h1>;
    }
    ```

2. **Class Components:** You can also use ES6 class to define a component. The above function component can be written as a class component:

    ```jsx
    class Greeting extends React.Component {
        render() {
            return <h1>{`Hello, ${this.props.message}`}</h1>;
        }
    }
    ```

========== Id ==========  
6

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#6-How-to-create-components-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
