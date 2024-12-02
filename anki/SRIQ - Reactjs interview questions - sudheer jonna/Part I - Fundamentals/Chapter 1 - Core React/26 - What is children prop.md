========== Question ==========  

### What is children prop?  

========== Answer ==========  

_Children_ is a prop that allows you to pass components as data to other components, just like any other prop you use. Component tree put between component's opening and closing tag will be passed to that component as `children` prop.

A simple usage of children prop looks as below,

```jsx
function MyDiv({ children }){
    return (
      <div>
        {children}
      </div>;
    );
}

export default function Greeting() {
  return (
    <MyDiv>
      <span>{"Hello"}</span>
      <span>{"World"}</span>
    </MyDiv>
  );
}
```

<details><summary><b>See Class</b></summary>

<p>

```jsx
const MyDiv = React.createClass({
    render: function () {
        return <div>{this.props.children}</div>;
    },
});

ReactDOM.render(
    <MyDiv>
        <span>{'Hello'}</span>
        <span>{'World'}</span>
    </MyDiv>,
    node,
);
```

</p>

</details>

**Note:** There are several methods available in the legacy React API to work with this prop. These include `React.Children.map`, `React.Children.forEach`, `React.Children.count`, `React.Children.only`, `React.Children.toArray`.

========== Id ==========  
26

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#26-What-is-children-prop

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
