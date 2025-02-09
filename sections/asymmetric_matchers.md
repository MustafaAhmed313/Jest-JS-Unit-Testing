#### Jest Asymmetric Matchers :

`expect.anything()` : is an asymmetric matcher that matches anything that is not equal to `undefined` or `null` and it's used with the `toEqual()` matcher.

```javascript
it('Testing anything...', () => {
  // Pass
  expect(sayJest()).toEqual(expect.anything());
  // Fail
  expect(null).toEqual(expect.anything());
});
```

> **Note:** each `expect()` call represents a partial test of the unit test. it means that a test will pass, if all the partial tests passed. The previous test will fail.

`expect.any()` : is an asymmetric matcher that takes a `constructor` and matches any object which is created via the received constructor.

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

it('Testing any...', () => {
  expect(new Person('mustafa', 21))
    .toEqual(expect.any(Person));
});
```

`expect.arrayContaining()` : is an asymmetric matcher that checks whether a given sub array that holds items which are contained in another array.

```javascript
it('Testing arrayContaining...', () => {
  expect([1, 2, 4, 5, 4])
    .toEqual(expect.arrayContaining([4, 4]));
});
```

> **Note:** the previous test is same as we replace `[4, 4]` by `[4, 4, 4, .....]` it will pass, because once the item is contained in the array then it passed. `(ex: a number 4 is contained two times in the array but, it doesn't mean that we match its occurrences)`

---

⬅️ [`previous`](../sections/utilities.md)
➡️ [`next`](../sections/code_coverage.md)
🚪[`index`](../README.md)