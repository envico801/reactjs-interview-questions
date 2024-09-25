========== Question ==========  

### What are capture phase events?  

========== Answer ==========  

The `onClickCapture` React event is helpful to catch all the events of child
elements irrespective of event propagation logic or even if the events
propagation stopped. This is useful if you need to log every click events for
analytics purpose.

For example, the below code triggers the click event of parent first followed by
second level child eventhough leaf child button elements stops the propagation.

```jsx
<div onClickCapture={() => alert('parent')}>
    <div onClickCapture={() => alert('child')}>
        <button onClick={(e) => e.stopPropagation()} />
        <button onClick={(e) => e.stopPropagation()} />
    </div>
</div>
```

The event propagation for the above code snippet happens in the following order:

1.  It travels downwards in the DOM tree by calling all `onClickCapture` event
    handlers.

2.  It executes `onClick` event handler on the target element.

3.  It travels upwards in the DOM tree by call all `onClick` event handlers
    above to it.

========== Id ==========  
251

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 8 - Miscellaneous

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-8-Miscellaneous::#251-What-are-capture-phase-events

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
