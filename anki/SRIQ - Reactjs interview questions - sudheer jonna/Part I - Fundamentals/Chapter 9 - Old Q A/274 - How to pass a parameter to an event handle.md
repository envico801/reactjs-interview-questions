========== Question ==========  

### How to pass a parameter to an event handler or callback?  

========== Answer ==========  

You can use an _arrow function_ to wrap around an _event handler_ and pass parameters:

```jsx
<button onClick={() => this.handleClick(id)} />
```

This is an equivalent to calling `.bind`:

```jsx
<button onClick={this.handleClick.bind(this, id)} />
```

Apart from these two approaches, you can also pass arguments to a function which is defined as arrow function

```jsx
<button onClick={this.handleClick(id)} />;
handleClick = (id) => () => {
    console.log('Hello, your ticket number is', id);
};
```

========== Id ==========  
274

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#274-How-to-pass-a-parameter-to-an-event-handle

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
