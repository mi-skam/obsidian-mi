---
created: 2024-01-07
modified: 2024-09-03T18:02:44+02:00
---
## from
 
The **`Array.from()`** static method creates a new, shallow-copied `Array` instance from an [iterable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols#the_iterable_protocol) or [array-like](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections#working_with_array-like_objects) object.

Helpful, if something is similar to a Array, but not exactly an Array, like `NodeList`

Interesting to create sequences, like an Array of 5 zeros

```js
Array.from({ length: 5 }, (_) => 0); // -> [0, 0, 0, 0, 0]
```

or the first numbers from 1 to 10

```js
Array.from({ length: 10 }, (_, idx) => idx + 1);
```

## find vs. [[1 - Inbox/Filter]]

both [[JS Arrays|Array]] methods create selections from an array. While `.filter()` creates a new Array with zero, one or many entries, `.find()` returns with the first found entry.

```js
const numbers = [1, 2, 3, 4, 5, 6];
const isEven = (num) => num % 2 === 0;

const evenNumbers = numbers.filter(isEven);
const firstEvenNumber = numbers.find(isEven);
```

## forEach, map, [[1 - Inbox/Reduce]]

We use these three functions for a [[1 - Inbox/Functional Style]]