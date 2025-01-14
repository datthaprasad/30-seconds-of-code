---
title: rangeGenerator
tags: function,generator,advanced
---

Creates a generator, that generates all values in the given range using the given step.

- Use a `while` loop to iterate from `start` to `end`, using `yield` to return each value and then incrementing by `step`.
- Omit the third argument, `step`, to use a default value of `1`.

```js
const rangeGenerator = function* (start, end) {
  let i = start;
  while (i < end) {
    yield i;
    i += 1;
  }
};
```

```js
for (let i of rangeGenerator(6, 10)) console.log(i);
// Logs 6, 7, 8, 9
```
