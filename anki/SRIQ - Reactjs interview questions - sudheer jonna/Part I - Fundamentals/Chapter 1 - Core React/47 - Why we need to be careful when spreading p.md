========== Question ==========  

### Why we need to be careful when spreading props on DOM elements?  

========== Answer ==========  

When we _spread props_ we run into the risk of adding unknown HTML attributes,
which is a bad practice. Instead we can use prop destructuring with `...rest`
operator, so it will add only required props.

For example,

```jsx
const ComponentA = () => (
    <ComponentB isDisplay={true} className={'componentStyle'} />
);
const ComponentB = ({ isDisplay, ...domProps }) => (
    <div {...domProps}>{'ComponentB'}</div>
);
```

========== Id ==========  
47

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#47-Why-we-need-to-be-careful-when-spreading-p

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
