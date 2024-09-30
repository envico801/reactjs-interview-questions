========== Question ==========  

### How to access current locale with React Intl?  

========== Answer ==========  

You can get the current locale in any component of your application using `injectIntl()`:

```jsx
import { injectIntl, intlShape } from 'react-intl';
const MyComponent = ({ intl }) => (
    <div>{`The current locale is ${intl.locale}`}</div>
);
MyComponent.propTypes = {
    intl: intlShape.isRequired,
};
export default injectIntl(MyComponent);
```

========== Id ==========  
94

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#94-How-to-access-current-locale-with-react-in

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
