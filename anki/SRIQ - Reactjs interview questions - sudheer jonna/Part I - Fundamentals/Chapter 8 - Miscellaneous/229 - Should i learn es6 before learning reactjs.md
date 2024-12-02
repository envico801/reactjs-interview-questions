========== Question ==========  

### Should I learn ES6 before learning ReactJS?  

========== Answer ==========  

No, you don’t have to learn es2015/es6 to learn react. But you may find many resources or React ecosystem uses ES6 extensively. Let's see some of the frequently used ES6 features,

1.  **Destructuring:** To get props and use them in a component

    ```javascript
    // in es 5
    var someData = this.props.someData;
    var dispatch = this.props.dispatch;
    // in es6
    const { someData, dispatch } = this.props;
    ```

2.  **Spread operator:** Helps in passing props down into a component

    ```javascript
    // in es 5
    <SomeComponent someData={this.props.someData} dispatch={this.props.dispatch} />
    // in es6
    <SomeComponent {...this.props} />
    ```

3.  **Arrow functions:** Makes compact syntax

    ```javascript
    // es 5
    var users = usersList.map(function (user) {
        return <li>{user.name}</li>;
    });
    // es 6
    const users = usersList.map((user) => <li>{user.name}</li>);
    ```

========== Id ==========  
229

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#229-Should-i-learn-es6-before-learning-reactjs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
