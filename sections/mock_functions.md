#### Jest Mock Functions :

`Mock functions` : are also known as "spies", because they let you spy on the behavior of a function that is called indirectly by some other code, rather than only testing the output.
we can create a mock function using `jest.fn()` which returns `undefined` by default.

```javascript
const { mock } = require('../index');

test('Testing mock function...', () => {
// Mock Function
  const mock = jest.fn((name) => {
    return `Hello ${name}`;
  });
 
  expect(mock('Mustafa')).toBe('Hello Mustafa');
  expect(mock('Ahmed')).toBe('Hello Ahmed');
  expect(mock('Mohamed')).toBe('Hello Mohamed');

  expect(mock).toHaveBeenCalled(); // at least one call
  expect(mock).toHaveBeenCalledTimes(3); // exactly have been called 3 times
  expect(mock).toHaveBeenCalledWith('Ahmed'); // is called with argument Ahmed
  expect(mock).toHaveBeenLastCalledWith('Mohamed'); // last call with Mohamed
});
```

here you can go in deep with [mock functions](https://jestjs.io/docs/mock-function-api).

---