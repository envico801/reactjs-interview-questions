========== Question ==========  

### Why do we use array destructuring (square brackets notation) in `useState`?  

========== Answer ==========  

When we declare a state variable with `useState`, it returns a pair — an array
with two items. The first item is the current value, and the second is a
function that updates the value. Using [0] and [1] to access them is a bit
confusing because they have a specific meaning. This is why we use array
destructuring instead.

For example, the array index access would look as follows:

```javascript
var userStateVariable = useState('userProfile'); // Returns an array pair
var user = userStateVariable[0]; // Access first item
var setUser = userStateVariable[1]; // Access second item
```

Whereas with array destructuring the variables can be accessed as follows:

```javascript
const [user, setUser] = useState('userProfile');
```

========== Id ==========  
220

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#220-Why-do-we-use-array-destructuring-square

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
