========== Question ==========  

### Must prop be named as render for render props?  

========== Answer ==========  

Even though the pattern named render props, you don’t have to use a prop named render to use this pattern. i.e, Any prop that is a function that a component uses to know what to render is technically a “render prop”. Lets take an example with the children prop for render props,

```javascript
<Mouse
    children={(mouse) => (
        <p>
            The mouse position is {mouse.x}, {mouse.y}
        </p>
    )}
/>
```

Actually children prop doesn’t need to be named in the list of “attributes” in JSX element. Instead, you can keep it directly inside element,

```javascript
<Mouse>
    {(mouse) => (
        <p>
            The mouse position is {mouse.x}, {mouse.y}
        </p>
    )}
</Mouse>
```

While using this above technique(without any name), explicitly state that children should be a function in your propTypes.

```javascript
Mouse.propTypes = {
    children: PropTypes.func.isRequired,
};
```

========== Id ==========  
205

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#205-Must-prop-be-named-as-render-for-render-pr

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
