========== Question ==========  

### What is context?  

========== Answer ==========  

_Context_ provides a way to pass data through the component tree without having
to pass props down manually at every level.

For example, authenticated users, locale preferences, UI themes need to be
accessed in the application by many components.

```javascript
const { Provider, Consumer } = React.createContext(defaultValue);
```

========== Id ==========  
283

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#283-What-is-context

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
