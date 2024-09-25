========== Question ==========  

### What is the use of the `ownProps` parameter in `mapStateToProps()` and `mapDispatchToProps()`?  

========== Answer ==========  

If the `ownProps` parameter is specified, React Redux will pass the props that
were passed to the component into your _connect_ functions. So, if you use a
connected component:

```jsx
import ConnectedComponent from './containers/ConnectedComponent';
<ConnectedComponent user={'john'} />;
```

The `ownProps` inside your `mapStateToProps()` and `mapDispatchToProps()`
functions will be an object:

```javascript
{
    user: 'john';
}
```

You can use this object to decide what to return from those functions.

========== Id ==========  
120

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 5 - React Redux

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-5-React-Redux::#120-What-is-the-use-of-the-ownprops-paramete

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
