========== Question ==========  

### What is Shallow Renderer in React testing?  

========== Answer ==========  

_Shallow rendering_ is useful for writing unit test cases in React. It lets you render a component _one level deep_ and assert facts about what its render method returns, without worrying about the behavior of child components, which are not instantiated or rendered.

For example, if you have the following component:

```javascript
function MyComponent() {
    return (
        <div>
            <span className={'heading'}>{'Title'}</span>
            <span className={'description'}>{'Description'}</span>
        </div>
    );
}
```

Then you can assert as follows:

```jsx
import ShallowRenderer from 'react-test-renderer/shallow';
// in your test
const renderer = new ShallowRenderer();
renderer.render(<MyComponent />);
const result = renderer.getRenderOutput();
expect(result.type).toBe('div');
expect(result.props.children).toEqual([
    <span className={'heading'}>{'Title'}</span>,
    <span className={'description'}>{'Description'}</span>,
]);
```

========== Id ==========  
96

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 4 - React Testing

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-4-React-Testing::#96-What-is-shallow-renderer-in-react-testing

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
