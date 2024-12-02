========== Question ==========  

### How do you render Array, Strings and Numbers in React 16 Version?  

========== Answer ==========  

**Arrays**: Unlike older releases, you don't need to make sure **render** method return a single element in React16. You are able to return multiple sibling elements without a wrapping element by returning an array.

For example, let us take the below list of developers,

```jsx
const ReactJSDevs = () => {
    return [
        <li key='1'>John</li>,
        <li key='2'>Jackie</li>,
        <li key='3'>Jordan</li>,
    ];
};
```

You can also merge this array of items in another array component.

```jsx
const JSDevs = () => {
    return (
        <ul>
            <li>Brad</li>
            <li>Brodge</li>
            <ReactJSDevs />
            <li>Brandon</li>
        </ul>
    );
};
```

**Strings and Numbers:** You can also return string and number type from the render method.

```jsx
render() {
 return 'Welcome to ReactJS questions';
}
// Number
render() {
 return 2018;
}
```

========== Id ==========  
167

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#167-How-do-you-render-array-strings-and-numbe

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
