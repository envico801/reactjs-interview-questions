========== Question ==========  

### What is the recommended way for naming components?  

========== Answer ==========  

It is recommended to name the component by reference instead of using `displayName`.

Using `displayName` for naming component:

```javascript
export default React.createClass({
    displayName: 'TodoApp',
    // ...
});
```

The **recommended** approach:

```javascript
export default class TodoApp extends React.Component {
    // ...
}
```

also

```javascript
const TodoApp = () => {
    //...
};
export default TodoApp;
```

========== Id ==========  
299

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#299-What-is-the-recommended-way-for-naming-com

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
