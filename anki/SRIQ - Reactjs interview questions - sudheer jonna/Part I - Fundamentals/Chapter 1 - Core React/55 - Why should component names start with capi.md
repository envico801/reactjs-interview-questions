========== Question ==========  

### Why should component names start with capital letter?  

========== Answer ==========  

If you are rendering your component using JSX, the name of that component has to begin with a capital letter otherwise React will throw an error as an unrecognized tag. This convention is because only HTML elements and SVG tags can begin with a lowercase letter.

```jsx
function SomeComponent {
  // Code goes here
}
```

You can define function component whose name starts with lowercase letter, but when it's imported it should have a capital letter. Here lowercase is fine:

```jsx
function myComponent {
  render() {
    return <div />;
  }
}

export default myComponent;
```

While when imported in another file it should start with capital letter:

```jsx
import MyComponent from './myComponent';
```

========== Id ==========  
55

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#55-Why-should-component-names-start-with-capi

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
