========== Question ==========  

### What are default props?  

========== Answer ==========  

The _defaultProps_ can be defined as a property on the component to set the
default values for the props. These default props are used when props not
supplied(i.e., undefined props), but not for `null` or `0` as props. That means,
If you provide null value then it remains null value. It's the same behavior
with 0 as well.

For example, let us create color default prop for the button component,

```javascript
function MyButton {
  // ...
}
MyButton.defaultProps = {
  color: "red",
};
```

If `props.color` is not provided then it will set the default value to 'red'.
i.e, Whenever you try to access the color prop it uses the default value

```javascript
function MyButton() {
    return <MyButton />; // props.color will contain red value
}
```

========== Id ==========  
178

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#178-What-are-default-props

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
