========== Question ==========  

### How do you say that props are readonly?  

========== Answer ==========  

When you declare a component as a function or a class, it must never modify its
own props.

Let us take a below capital function,

```javascript
function capital(amount, interest) {
    return amount + interest;
}
```

The above function is called “pure” because it does not attempt to change their
inputs, and always return the same result for the same inputs. Hence, React has
a single rule saying "All React components must act like pure functions with
respect to their props."

========== Id ==========  
190

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#190-How-do-you-say-that-props-are-readonly

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
