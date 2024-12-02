========== Question ==========  

### What are React Mixins?  

========== Answer ==========  

_Mixins_ are a way to totally separate components to have a common functionality. Mixins **should not be used** and can be replaced with _higher-order components_ or _decorators_.

One of the most commonly used mixins is `PureRenderMixin`. You might be using it in some components to prevent unnecessary re-renders when the props and state are shallowly equal to the previous props and state:

```javascript
const PureRenderMixin = require('react-addons-pure-render-mixin');

const Button = React.createClass({
    mixins: [PureRenderMixin],
    // ...
});
```

 <!-- TODO: mixins are deprecated -->

========== Id ==========  
53

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#53-What-are-react-mixins

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
