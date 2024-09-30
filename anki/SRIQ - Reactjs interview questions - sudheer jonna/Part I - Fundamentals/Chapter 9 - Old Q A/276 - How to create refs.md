========== Question ==========  

### How to create refs?  

========== Answer ==========  

There are two approaches

1. This is a recently added approach. _Refs_ are created using `React.createRef()` method and attached to React elements via the `ref` attribute. In order to use _refs_ throughout the component, just assign the _ref_ to the instance property within constructor.

```jsx
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        this.myRef = React.createRef();
    }
    render() {
        return <div ref={this.myRef} />;
    }
}
```

2. You can also use ref callbacks approach regardless of React version. For example, the search bar component's input element is accessed as follows,

```jsx
class SearchBar extends Component {
    constructor(props) {
        super(props);
        this.txtSearch = null;
        this.state = { term: '' };
        this.setInputSearchRef = (e) => {
            this.txtSearch = e;
        };
    }
    onInputChange(event) {
        this.setState({ term: this.txtSearch.value });
    }
    render() {
        return (
            <input
                value={this.state.term}
                onChange={this.onInputChange.bind(this)}
                ref={this.setInputSearchRef}
            />
        );
    }
}
```

You can also use _refs_ in function components using **closures**.

**Note**: You can also use inline ref callbacks even though it is not a recommended approach.

========== Id ==========  
276

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#276-How-to-create-refs

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
