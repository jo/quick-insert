# Quick Insert
Simple quicksort-style array insertion function.

[![Build Status](https://travis-ci.org/jo/quick-insert.svg?branch=master)](https://travis-ci.org/jo/quick-insert)

Based on
http://stackoverflow.com/questions/3423394/algorithm-of-javascript-sort-function

## Usage
```js
var quickInsert = require('quick-insert')

var numbers = [1,3];
quickInsert(2, numbers)
// [1,2,3]

var objects = [
  { n: 1 },
  { n: 3 }
];
quickInsert({ n: 2 }, objects, function(a, b) {
  if (a.n === b.n) return 0;
  return a.n < b.n ? -1 : 1;
})
// [
//   { n: 1 },
//   { n: 2 },
//   { n: 3 }
// ]
```
