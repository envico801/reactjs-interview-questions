========== Question ==========  

### How to format date using React Intl?  

========== Answer ==========  

The `injectIntl()` higher-order component will give you access to the `formatDate()` method via the props in your component. The method is used internally by instances of `FormattedDate` and it returns the string representation of the formatted date.

```jsx
import { injectIntl, intlShape } from 'react-intl';

const stringDate = this.props.intl.formatDate(date, {
    year: 'numeric',
    month: 'numeric',
    day: 'numeric',
});

const MyComponent = ({ intl }) => (
    <div>{`The formatted date is ${stringDate}`}</div>
);

MyComponent.propTypes = {
    intl: intlShape.isRequired,
};

export default injectIntl(MyComponent);
```

========== Id ==========  
95

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#95-How-to-format-date-using-react-intl

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
