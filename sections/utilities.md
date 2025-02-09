#### Jest Utilities :

`expect.extend()` : is a utility allows you to add custom matchers and use them on any unit test in the `file.test.js`.

```javascript
expect.extend({
  toBeJest(received) {
    const pass = received === `Jest`;
    if (pass) {
      return {
        message: () => 'The received is Jest',
        pass: true
      };
    } else {
      return {
        message: () => `Error: The received ${received} is not Jest`,
        pass: false
      };
    }
  }
});

it('Testing toBeJest Matcher...', () => {
  expect(sayJest()).toBeJest();
});
```

Any matcher in Jest returns an object has two fundamental properties `message` which is a function returns a string message, and `pass` which is a truth value indicates whether the test passed or failed.

> **Note:** the `expect().not` modifier negates the `pass` property by returning its bang `!pass`.

> **Note:** the `received` object doesn't belong to the matcher method explicitly but, belongs to the return of `expect(something)` as it's the return value of the `something`. you can add a parameter `(ex: target)` to your matcher method that mean your matcher accepts one parameter called `target`.

---

⬅️ [`previous`](../sections/matchers.md)
➡️ [`next`](../sections/asymmetric_matchers.md)
🚪[`index`](../README.md)