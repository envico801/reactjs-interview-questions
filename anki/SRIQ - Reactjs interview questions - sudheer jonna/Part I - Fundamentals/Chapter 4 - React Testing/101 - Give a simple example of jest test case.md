========== Question ==========  

### Give a simple example of Jest test case  

========== Answer ==========  

Let's write a test for a function that adds two numbers in `sum.js` file:

```javascript
const sum = (a, b) => a + b;

export default sum;
```

Create a file named `sum.test.js` which contains actual test:

```javascript
import sum from './sum';

test('adds 1 + 2 to equal 3', () => {
    expect(sum(1, 2)).toBe(3);
});
```

And then add the following section to your `package.json`:

```json
{
    "scripts": {
        "test": "jest"
    }
}
```

Finally, run `yarn test` or `npm test` and Jest will print a result:

```console
$ yarn test
PASS ./sum.test.js
✓ adds 1 + 2 to equal 3 (2ms)
```

========== Id ==========  
101

---

DECK INFO

TARGET DECK: Javascript::Interview::SRIQ - Reactjs interview questions - sudheer jonna::Part I - Fundamentals::Chapter 4 - React Testing

FILE TAGS: #Javascript::#Interview::#SRIQ-Reactjs-interview-questions-sudheer-jonna::#Part-I-Fundamentals::#Chapter-4-React-Testing::#101-Give-a-simple-example-of-jest-test-case

Tags:

Reference:

Related:

```dataview
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
