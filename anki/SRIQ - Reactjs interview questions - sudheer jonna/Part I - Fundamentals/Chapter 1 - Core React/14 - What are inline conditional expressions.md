========== Question ==========  

### What are inline conditional expressions?  

========== Answer ==========  

You can use either _if statements_ or _ternary expressions_ which are available
from JS to conditionally render expressions. Apart from these approaches, you
can also embed any expressions in JSX by wrapping them in curly braces and then
followed by JS logical operator `&&`.

```jsx
<h1>Hello!</h1>;
{
    messages.length > 0 && !isLogin ?
        <h2>You have {messages.length} unread messages.</h2>
    :   <h2>You don't have unread messages.</h2>;
}
```

========== Id ==========  
14

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#14-What-are-inline-conditional-expressions

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
