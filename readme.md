## javascript-charlike-snippets

> My SublimeText 2/3 snippets. From BDD through `assert` to singleton pattern, es6 fat arrows and es6 import


## Rebuilding
```
zip javascript-charlike-snippets.sublime-package -r javascript-charlike-snippets && \
cp javascript-charlike-snippets.sublime-package ~/.config/sublime-text-3/Installed\ Packages/
```

### module system

- **[rr]** node require
```js
var pkg = require('package');
```

- **[imp]** javascript import
```js
import pkg from 'package';
```

### functions and arrows

- **[fat]** es6 arrow
```js
(args) => 
```

- **[ofat]** es6 arrow as object property
```js
name: (args) => 
```

- **[me]** module.exports - named function
```js
module.exports = function named(args) {
  // body
};
```

- **[mea]** module.exports - anonymous function
```js
module.exports = function(args) {
  // body
};
```

- **[fn]** named function
```js
function name(args) {
  
}
```

- **[afn]** anonymous function
```js
function(args) {
  
}
```

- **[ofn]** anonymous function as object property
```js
name: function name(args) {
  
}
```

- **[oafn]** anonymous function as object property
```js
name: function(args) {
  
}
```

### assert

- **[ase]** assert equal
```js
assert.equal(actual, expected, msg);
```

- **[asn]** assert notEqual
```js
assert.notEqual(actual, expected, msg);
```

- **[asse]** assert strictEqual
```js
assert.strictEqual(actual, expected, msg);
```

- **[assn]** assert notStrictEqual
```js
assert.notStrictEqual(actual, expected, msg);
```

- **[asd]** assert deepEqual
```js
assert.deepEqual(actual, expected, msg);
```

- **[asdn]** assert notDeepEqual
```js
assert.notDeepEqual(actual, expected, msg);
```

- **[assd]** assert.deepStrictEqual
```js
assert.deepStrictEqual(actual, expected, msg);
```

- **[assdn]** assert.notDeepStrictEqual
```js
assert.notDeepStrictEqual(actual, expected, msg);
```

- **[ast]** assert.throws
```js
assert.throws(actual, expected, msg);
```

- **[asi]** assert.ifError
```js
assert.ifError(actual, expected, msg);
```

### testing

- **[desc]** describe
```js
describe('description', function() {
  // body
});
```

- **[ita]** it async
```js
it('description', function(done) {
  // body
  done();
});
```

### console and misc

- **[cl]** console.log
```js
console.log(actual);
```

- **[ce]** console.error
```js
console.error(actual);
```

- **[self]** self this
```js
var self = this;
```

- **[us]** use strict
```js
'use strict';
```

- **[singleton]** singleton pattern
```js
function ClassName(options) {
  if (!(this instanceof ClassName)) {
    return new ClassName(options);
  }
  // body
}
```



## Author
**Charlike Mike Reagent**
+ [gratipay/tunnckoCore][author-gratipay]
+ [twitter/tunnckoCore][author-twitter]
+ [github/tunnckoCore][author-github]
+ [npmjs/tunnckoCore][author-npmjs]
+ [more ...][contrib-more]


## License [![MIT license][license-img]][license-url]
Copyright (c) 2015 [Charlike Mike Reagent][contrib-more], [contributors][contrib-graf].  
Released under the [`MIT`][license-url] license.


[npmjs-url]: http://npm.im/blitzcrank
[npmjs-img]: https://img.shields.io/npm/v/blitzcrank.svg?style=flat&label=blitzcrank

[coveralls-url]: https://coveralls.io/r/tunnckoCore/blitzcrank?branch=master
[coveralls-img]: https://img.shields.io/coveralls/tunnckoCore/blitzcrank.svg?style=flat

[license-url]: https://github.com/tunnckoCore/blitzcrank/blob/master/license.md
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg?style=flat

[travis-url]: https://travis-ci.org/tunnckoCore/blitzcrank
[travis-img]: https://img.shields.io/travis/tunnckoCore/blitzcrank.svg?style=flat

[daviddm-url]: https://david-dm.org/tunnckoCore/blitzcrank
[daviddm-img]: https://img.shields.io/david/tunnckoCore/blitzcrank.svg?style=flat

[author-gratipay]: https://gratipay.com/tunnckoCore
[author-twitter]: https://twitter.com/tunnckoCore
[author-github]: https://github.com/tunnckoCore
[author-npmjs]: https://npmjs.org/~tunnckocore

[contrib-more]: http://j.mp/1stW47C
[contrib-graf]: https://github.com/tunnckoCore/blitzcrank/graphs/contributors

***

_Powered and automated by [kdf](https://github.com/tunnckoCore), March 22, 2015_