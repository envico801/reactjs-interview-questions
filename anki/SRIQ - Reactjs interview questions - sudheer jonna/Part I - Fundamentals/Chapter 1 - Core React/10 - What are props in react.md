========== Question ==========  

### What are props in React?  

========== Answer ==========  

_Props_ are inputs to components. They are single values or objects containing a set of values that are passed to components on creation similar to HTML-tag attributes. Here, the data is passed down from a parent component to a child component.

The primary purpose of props in React is to provide following component functionality:

1. Pass custom data to your component.

2. Trigger state changes.

3. Use via `this.props.reactProp` inside component's `render()` method.

For example, let us create an element with `reactProp` property:

```jsx
<Element reactProp={'1'} />
```

This `reactProp` (or whatever you came up with) attribute name then becomes a property attached to React's native props object which originally already exists on all components created using React library.

```jsx
props.reactProp;
```

For example, the usage of props in function component looks like below:

```jsx
import React from 'react';
import ReactDOM from 'react-dom';

const ChildComponent = (props) => {
    return (
        <div>
            <p>{props.name}</p>
            <p>{props.age}</p>
            <p>{props.gender}</p>
        </div>
    );
};

const ParentComponent = () => {
    return (
        <div>
            <ChildComponent name='John' age='30' gender='male' />
            <ChildComponent name='Mary' age='25' geneder='female' />
        </div>
    );
};
```

The properties from props object can be accessed directly using destructing feature from ES6 (ECMAScript 2015). It is also possible to fallback to default value when the prop value is not specified. The above child component can be simplified like below.

```jsx
const ChildComponent = ({ name, age, gender = 'male' }) => {
    return (
        <div>
            <p>{name}</p>
            <p>{age}</p>
            <p>{gender}</p>
        </div>
    );
};
```

**Note:** The default value won't be used if you pass `null` or `0` value. i.e, default value is only used if the prop value is missed or `undefined` value has been passed.

  <details><summary><b>See Class</b></summary>

The Props accessed in Class Based Component as below

```jsx
import React from 'react';
import ReactDOM from 'react-dom';

class ChildComponent extends React.Component {
    render() {
        return (
            <div>
                <p>{this.props.name}</p>
                <p>{this.props.age}</p>
                <p>{this.props.gender}</p>
            </div>
        );
    }
}

class ParentComponent extends React.Component {
    render() {
        return (
            <div>
                <ChildComponent name='John' age='30' gender='male' />
                <ChildComponent name='Mary' age='25' gender='female' />
            </div>
        );
    }
}
```

  </details>

========== Id ==========  
10

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#10-What-are-props-in-react

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
