========== Question ==========  

### What is dynamic import?  

========== Answer ==========  

You can achieve code-splitting in your app using dynamic import.

Let's take an example of addition,

1.  **Normal Import**

```javascript
import { add } from './math';
console.log(add(10, 20));
```

2.  **Dynamic Import**

```javascript
import('./math').then((math) => {
    console.log(math.add(10, 20));
});
```

========== Id ==========  
197

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#197-What-is-dynamic-import

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
