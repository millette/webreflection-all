# @webreflection/all

[![Coverage Status](https://coveralls.io/repos/github/WebReflection/all/badge.svg?branch=main)](https://coveralls.io/github/WebReflection/all?branch=main)

<sup>**Social Media Photo by [Julie Pittevils](https://unsplash.com/@juliepittevils) on [Unsplash](https://unsplash.com/)**</sup>

- - -

### ⚠️ Maintained Elsewhere

This module is definitevely too small to be a package a part so it's been moved into https://github.com/WebReflection/utils and it's reachable via *CDN* as `https://esm.run/@webreflection/utils/all` or by any other usual mean.

- - -

Tiny `Promise.all` companion with one extra convenience: when called with a
single object literal, it resolves each value and returns an object with the
same keys.

```js
import all from '@webreflection/all';

const user = await all({
  name: fetchName(),
  age: fetchAge()
});

// { name: 'Ada', age: 36 }
```

This preserves the shape and names of object-literal work, avoiding the
positional array juggling required by `Promise.all`. For arrays, or for two or
more arguments, it behaves like `Promise.all` and resolves to an array.
