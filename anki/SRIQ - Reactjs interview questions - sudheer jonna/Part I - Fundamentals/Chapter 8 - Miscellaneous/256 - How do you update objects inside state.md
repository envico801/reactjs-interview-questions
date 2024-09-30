========== Question ==========  

### How do you update objects inside state?  

========== Answer ==========  

You cannot update the objects which exists in the state directly. Instead, you should create a fresh new object (or copy from the existing object) and update the latest state using the newly created object. Eventhough JavaScript objects are mutable, you need to treat objects inside state as read-only while updating the state.

Let's see this comparison with an example. The issue with regular object mutation approach can be described by updating the user details fields of `Profile` component. The properties of `Profile` component such as firstName, lastName and age details mutated in an event handler as shown below.

```jsx
import { useState } from 'react';
export default function Profile() {
    const [user, setUser] = useState({
        firstName: 'John',
        lastName: 'Abraham',
        age: 30,
    });
    function handleFirstNameChange(e) {
        user.firstName = e.target.value;
    }
    function handleLastNameChange(e) {
        user.lastName = e.target.value;
    }
    function handleAgeChange(e) {
        user.age = e.target.value;
    }
    return (
        <>
            <label>
                First name:
                <input
                    value={user.firstName}
                    onChange={handleFirstNameChange}
                />
            </label>
            <label>
                Last name:
                <input value={user.lastName} onChange={handleLastNameChange} />
            </label>
            <label>
                Age:
                <input value={user.age} onChange={handleAgeChange} />
            </label>
            <p>
                Profile:
                {person.firstName} {person.lastName} ({person.age})
            </p>
        </>
    );
}
```

Once you run the application with above user profile component, you can observe that user profile details won't be update upon entering the input fields.

This issue can be fixed by creating a new copy of object which includes existing properties through spread syntax(...obj) and add changed values in a single event handler itself as shown below.

```jsx
handleProfileChange(e) {
  setUser({
  ...user,
    [e.target.name]: e.target.value
  });
}
```

The above event handler is concise instead of maintaining separate event handler for each field. Now, UI displays the updated field values as expected without an issue.

========== Id ==========  
256

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#256-How-do-you-update-objects-inside-state

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
