#### Jest Matchers :

`toBe()` : is a matcher that matches a single value by another one.

```javascript
const list = [1, 2, 3];

it('Match the length of the list...', () => {
	expect(list.length).toBe(3);
});
```

`toHaveLength()` : is a matcher that checks whether the object has a length property and equal to some numeric value.

```javascript
const list = [1, 2, 3];

it('Match the length of the list...', () => {
	expect(list).toHaveLength(3);
});
```

`toContain()` :  is a matcher that checks whether the list contain the passwd item or the string is a substring from another one.

```javascript
const list = [1, 2, 3];

it('Match the length of the list...', () => {
	expect(list).toContain(3);
});

const string = 'mustafa';

it('Match the substring...', () => {
	expect(string).toContain('us');
});
```

> **Note:** you can use the `expect().not` modifier to negates the matcher functionality.

```javascript
const list = [1, 2, 3];

it('Match the length of the list...', () => {
	expect(list).not.toContain(0);
});
```

`toBeFalsy()` : is a matcher that checks whether the value is a `falsy` value, something like `undefined`, `null`, `[]`, `{}`, `0`, and `NaN` . `(i.e. expect the boolean result to be 0)`

```javascript
it('Match the falsy value...', () => {
	expect([]).toBeFalsy();
});
```

`toBeTruthy()` : is a matcher that checks whether the value is not a `falsy` value. `(i.e. expect the boolean result to be 1)`

```javascript
const list = [1, 2, 3];

it('Match the truthy value...', () => {
	expect(list).toBeTruthy();
});
```

`toBeGreaterThan()` : is a matcher that checks whether a given value is greater than another one.

```javascript
it('Testing greater than...', () => {
	expect(1).toBeGreaterThan(0);
});
```

`toBeGreaterThanOrEqual()` : is a matcher that checks whether a given value is greater than or equal another one.

```javascript
it('Testing greater than or equal...', () => {
	expect(0).toBeGreaterThanOrEqual(0);
});
```

`toBeLessThan()` : is a matcher that checks whether a given value is less than another one.

```javascript
it('Testing less than...', () => {
	expect(-1).toBeLessThan(0);
});
```

`toBeLessThanOrEqual()` : is a matcher that checks whether a given value is less than or equal another one.

```javascript
it('Testing less than or equal...', () => {
	expect(0).toBeLessThanOrEqual(0);
});
```

`toBeUndefined()` : is a matcher that checks whether a given value is equal to `undefined`.

```javascript
it('Testing unknown...', () => {
	let unknown;
	expect(unknown).toBeUndefined();
});
```

`toMatch()` : is a matcher that checks whether a given string matches a given regular expression `Regex`.

```javascript
it('Testing regex...', () => {
	let introduction = 'My name is Mustafa Ahmed';
	expect(introduction).toMatch(/Mustafa/);
});
```

`toHaveProperty()` : is a matcher that checks whether a given object contains some property with `(Optional)` some value.

```javascript
const me = {
	name: 'Mustafa Ahmed',
	age: 21
};

it('Testing name property...', () => {
	expect(me).toHaveProperty('name');
});

it('Testing name property value...', () => {
	expect(me).toHaveProperty('name', 'Mustafa Ahmed');
});
```

I think you have many ideas for more efficient matchers like combined matchers or even your own customized matcher. We will introduce the customized jest matchers in the nest section. see more built-in jest [matchers](https://jestjs.io/docs/expect#matchers).

---