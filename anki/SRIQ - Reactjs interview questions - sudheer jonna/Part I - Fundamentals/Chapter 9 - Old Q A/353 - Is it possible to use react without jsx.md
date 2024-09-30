========== Question ==========  

### Is it possible to use react without JSX?  

========== Answer ==========  

Yes, JSX is not mandatory for using React. Actually it is convenient when you don’t want to set up compilation in your build environment. Each JSX element is just syntactic sugar for calling `React.createElement(component, props, ...children)`.

For example, let us take a greeting example with JSX,

```javascript
class Greeting extends React.Component {
    render() {
        return <div>Hello {this.props.message}</div>;
    }
}
ReactDOM.render(<Greeting message='World' />, document.getElementById('root'));
```

You can write the same code without JSX as below,

```javascript
class Greeting extends React.Component {
    render() {
        return React.createElement('div', null, `Hello ${this.props.message}`);
    }
}
ReactDOM.render(
    React.createElement(Greeting, { message: 'World' }, null),
    document.getElementById('root'),
);
```

========== Id ==========  
353

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#353-Is-it-possible-to-use-react-without-jsx

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
