========== Question ==========  

### Does the statics object work with ES6 classes in React?  

========== Answer ==========  

No, `statics` only works with `React.createClass()`:

```javascript
someComponent = React.createClass({
    statics: {
        someMethod: function () {
            // ..
        },
    },
});
```

But you can write statics inside ES6+ classes as below,

```javascript
class Component extends React.Component {
    static propTypes = {
        // ...
    };
    static someMethod() {
        // ...
    }
}
```

or writing them outside class as below,

```javascript
class Component extends React.Component {
   ....
}
Component.propTypes = {...}
Component.someMethod = function(){....}
```

========== Id ==========  
324

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#324-Does-the-statics-object-work-with-es6-clas

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
