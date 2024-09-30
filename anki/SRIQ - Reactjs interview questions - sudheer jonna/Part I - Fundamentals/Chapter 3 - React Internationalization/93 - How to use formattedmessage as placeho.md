========== Question ==========  

### How to use `<FormattedMessage>` as placeholder using React Intl?  

========== Answer ==========  

The `<Formatted... />` components from `react-intl` return elements, not plain text, so they can't be used for placeholders, alt text, etc. In that case, you should use lower level API `formatMessage()`. You can inject the `intl` object into your component using `injectIntl()` higher-order component and then format the message using `formatMessage()` available on that object.

```jsx
import React from 'react';
import { injectIntl, intlShape } from 'react-intl';
const MyComponent = ({ intl }) => {
    const placeholder = intl.formatMessage({ id: 'messageId' });
    return <input placeholder={placeholder} />;
};
MyComponent.propTypes = {
    intl: intlShape.isRequired,
};
export default injectIntl(MyComponent);
```

========== Id ==========  
93

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 3 - React Internationalization

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-3-React-Internationalization::#93-How-to-use-formattedmessage-as-placeho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
