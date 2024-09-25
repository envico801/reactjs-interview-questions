========== Question ==========  

### How to dispatch an action on load?  

========== Answer ==========  

You can dispatch an action in `componentDidMount()` method and in `render()`
method you can verify the data.

```javascript
class App extends Component {
    componentDidMount() {
        this.props.fetchData();
    }
    render() {
        return this.props.isLoaded ?
                <div>{'Loaded'}</div>
            :   <div>{'Not Loaded'}</div>;
    }
}
const mapStateToProps = (state) => ({
    isLoaded: state.isLoaded,
});
const mapDispatchToProps = { fetchData };
export default connect(mapStateToProps, mapDispatchToProps)(App);
```

========== Id ==========  
320

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#320-How-to-dispatch-an-action-on-load

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
