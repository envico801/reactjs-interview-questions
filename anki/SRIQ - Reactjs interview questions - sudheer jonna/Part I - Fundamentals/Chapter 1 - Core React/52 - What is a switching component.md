========== Question ==========  

### What is a switching component?  

========== Answer ==========  

A _switching component_ is a component that renders one of many components. We need to use object to map prop values to components.

For example, a switching component to display different pages based on `page` prop:

```jsx
import HomePage from './HomePage';
import AboutPage from './AboutPage';
import ServicesPage from './ServicesPage';
import ContactPage from './ContactPage';

const PAGES = {
    home: HomePage,
    about: AboutPage,
    services: ServicesPage,
    contact: ContactPage,
};

const Page = (props) => {
    const Handler = PAGES[props.page] || ContactPage;

    return <Handler {...props} />;
};

// The keys of the PAGES object can be used in the prop types to catch dev-time errors.
Page.propTypes = {
    page: PropTypes.oneOf(Object.keys(PAGES)).isRequired,
};
```

========== Id ==========  
52

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 1 - Core React

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-1-Core-React::#52-What-is-a-switching-component

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
