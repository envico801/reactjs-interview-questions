========== Question ==========  

### What is the recommended ordering of methods in component class?  

========== Answer ==========  

_Recommended_ ordering of methods from _mounting_ to _render stage_:

1. `static` methods

2. `constructor()`

3. `getChildContext()`

4. `componentWillMount()`

5. `componentDidMount()`

6. `componentWillReceiveProps()`

7. `shouldComponentUpdate()`

8. `componentWillUpdate()`

9. `componentDidUpdate()`

10. `componentWillUnmount()`

11. click handlers or event handlers like `onClickSubmit()` or `onChangeDescription()`

12. getter methods for render like `getSelectReason()` or `getFooterContent()`

13. optional render methods like `renderNavigation()` or `renderProfilePicture()`

14. `render()`

========== Id ==========  
300

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 9 - Old Q A

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-9-Old-Q-A::#300-What-is-the-recommended-ordering-of-method

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
