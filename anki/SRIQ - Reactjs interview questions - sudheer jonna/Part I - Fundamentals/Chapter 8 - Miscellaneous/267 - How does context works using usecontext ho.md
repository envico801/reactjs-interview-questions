========== Question ==========  

### How does context works using useContext hook?  

========== Answer ==========  

The Context API in React, along with the `useContext` hook, provides a way to share data across multiple components without explicitly passing props through each level of the component tree. This is particularly useful for passing global data or for cases where many components need access to the same data.

Here's an overview of how context works with the `useContext` hook:

1. Create a context:

    First, you create a context using `React.createContext()`.

2. Provide the context:

    Wrap the parent component with a Context Provider to make the context available to all child components.

3. Consume the context:

    Use the `useContext` hook in any child component to access the context value.

Let's illustrate this with a simple example:

```javascript
import React, { createContext, useContext, useState } from 'react';
// Step 1: Create a context
const ThemeContext = createContext();
// Step 2: Create a provider component
const ThemeProvider = ({ children }) => {
    const [theme, setTheme] = useState('light');
    const toggleTheme = () => {
        setTheme((prevTheme) => (prevTheme === 'light' ? 'dark' : 'light'));
    };
    return (
        <ThemeContext.Provider value={{ theme, toggleTheme }}>
            {children}
        </ThemeContext.Provider>
    );
};
// Step 3: Create components that use the context
const ThemedButton = () => {
    const { theme, toggleTheme } = useContext(ThemeContext);
    return (
        <button
            onClick={toggleTheme}
            style={{
                backgroundColor: theme === 'light' ? '#fff' : '#333',
                color: theme === 'light' ? '#333' : '#fff',
            }}
        >
            Toggle Theme
        </button>
    );
};
const ThemedText = () => {
    const { theme } = useContext(ThemeContext);
    return (
        <p style={{ color: theme === 'light' ? '#333' : '#fff' }}>
            Current theme: {theme}
        </p>
    );
};
// Step 4: Use the provider to wrap the app
const App = () => {
    return (
        <ThemeProvider>
            <div>
                <h1>Theme Example</h1>
                <ThemedText />
                <ThemedButton />
            </div>
        </ThemeProvider>
    );
};
export default App;
```

Let's break down how this works:

1. We create a `ThemeContext` using `createContext()`.

2. The `ThemeProvider` component:

    - Manages the theme state.

    - Provides a function to toggle the theme.

    - Wraps its children with `ThemeContext.Provider`, passing the theme state and toggle function as the context value.

3. Child components (`ThemedButton` and `ThemedText`):

    - Use the `useContext` hook to access the theme context.

    - Can read the current theme and call the toggle function without these being passed as props.

4. The `App` component wraps everything in `ThemeProvider`, making the theme context available throughout the app.

Key benefits of using context with `useContext`:

1. Avoids prop drilling: You don't need to pass props through intermediate components.

2. Centralized state management: Useful for global states like themes, user authentication, language preferences, etc.

3. Component reusability: Components can be more easily reused as they're not tightly coupled to their data source.

4. Performance: Can potentially improve performance by reducing re-renders of intermediate components.

However, it's important to note that context should not be used for every type of state or prop. It's best suited for global or widely-used data. For local state or props that are only used by a few closely related components, regular state management or prop passing is often more appropriate.

========== Id ==========  
267

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#267-How-does-context-works-using-usecontext-ho

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
