========== Question ==========  

### How to bind methods or event handlers in JSX callbacks?  

========== Answer ==========  

There are 3 possible ways to achieve this in class components:

1. **Binding in Constructor:** In JavaScript classes, the methods are not bound
   by default. The same rule applies for React event handlers defined as class
   methods. Normally we bind them in constructor.

```javascript
class User extends Component {
    constructor(props) {
        super(props);
        this.handleClick = this.handleClick.bind(this);
    }
    handleClick() {
        console.log('SingOut triggered');
    }
    render() {
        return <button onClick={this.handleClick}>SingOut</button>;
    }
}
```

2. **Public class fields syntax:** If you don't like to use bind approach then
   _public class fields syntax_ can be used to correctly bind callbacks. The
   Create React App enables this syntax by default.

```jsx
handleClick = () => {
    console.log('SingOut triggered', this);
};
```

```jsx
<button onClick={this.handleClick}>SingOut</button>
```

3. **Arrow functions in callbacks:** It is possible to use _arrow functions_
   directly in the callbacks.

```jsx
handleClick() {
    console.log('SingOut triggered');
}
render() {
    return <button onClick={() => this.handleClick()}>SignOut</button>;
}
```

**Note:** If the callback is passed as prop to child components, those
components might do an extra re-rendering. In those cases, it is preferred to go
with `.bind()` or _public class fields syntax_ approach considering performance.

========== Id ==========  
273

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#273-How-to-bind-methods-or-event-handlers-in-j

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
