========== Question ==========  

### What are the preferred and non-preferred array operations for updating the state?  

========== Answer ==========  

The below table represent preferred and non-preferred array operations for updating the component state.

| Action    | Preferred            | Non-preferred              |
| --------- | -------------------- | -------------------------- |
| Adding    | concat, [...arr]     | push, unshift              |
| Removing  | filter, slice        | pop, shift, splice         |
| Replacing | map                  | splice, arr[i] = someValue |
| sorting   | copying to new array | reverse, sort              |

If you use Immer library then you can able to use all array methods without any problem.

========== Id ==========  
261

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#261-What-are-the-preferred-and-non-preferred-a

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
