## javascript-charlike-snippets

> My SublimeText 2/3 snippets. From BDD through `assert` to singleton pattern, es6 fat arrows and es6 import


## Rebuilding
```
zip javascript-charlike-snippets.sublime-package -r javascript-charlike-snippets && \
cp javascript-charlike-snippets.sublime-package ~/.config/sublime-text-3/Installed\ Packages/
```


## Code Style

[![standard][standard-image]][standard-url]

This snippets use [`standard`][standard-url] to maintain code style and consistency, and to avoid style arguments. You are encouraged to install it globally.

[standard-image]: https://cdn.rawgit.com/feross/standard/master/badge.svg
[standard-url]: https://github.com/feross/standard


## Table of Contents
- [module system](https://github.com/tunnckoCore/javascript-charlike-snippets#module-system)
  + `rr` node variable require
  + `req` node require
  + `imp` javascript import
- [functions-and-arrows](https://github.com/tunnckoCore/javascript-charlike-snippets#functions-and-arrows)
  + `fat` es6 arrow function
  + `ofat` es6 arrow function as object property
  + `me` module.exports
  + `men` module.exports - named function
  + `mea` module.exports - anonymous function
  + `fn` named function
  + `afn` anonymous function
  + `ofn` named function as object property
  + `oafn` anonymous function as object property
  + `fixture` fixture function (useful when assert.throws)
  + `iife` immediately-invoked function expression
- [assert](https://github.com/tunnckoCore/javascript-charlike-snippets#assert)
  + `ase` assert.equal
  + `asn` assert.notEqual
  + `asse` assert.strictEqual
  + `assn` assert.notStrictEqual
  + `asd` assert.deepEqual
  + `asdn` assert.notDeepEqual
  + `assd` assert.deepStrictEqual
  + `assdn` assert.notDeepStrictEqual
  + `asi` assert.ifError
  + `ast` assert.throws(actual, expected, msg)
  + `aste` assert.throws fixture Error
  + `asttype`  assert.throws fixture TypeError
  + `astre`  assert.throws fixture regexp message
- [testing](https://github.com/tunnckoCore/javascript-charlike-snippets#testing)
  + `desc` describe
  + `ita` it async
  + `its` it sync
- [console and misc](https://github.com/tunnckoCore/javascript-charlike-snippets#console-and-misc)
  + `cl` console.log
  + `ce` console.error
  + `self` self this
  + `us` use strict
  + `loop` fast while loop
  + `singleton` singleton pattern


### module system

- **[rr]** node variable require
```js
var ${2:pkg} = require('${1:package}')${0}
```

- **[req]** node require
```js
require('${1:package}')${0}
```

- **[imp]** javascript import
```js
import ${2:pkg} from '${1:package}'${0}
```

### functions and arrows

- **[fat]** es6 arrow
```js
(${1:args}) => ${0}
```

- **[ofat]** es6 arrow as object property
```js
${1:name}: (${2:args}) => ${0}
```

- **[me]** module.exports
```js
module.exports = ${0}
```

- **[men]** module.exports - named function
```js
module.exports = function ${1:name} (${2:args}) {
  ${0}
}
```

- **[mea]** module.exports - anonymous function
```js
module.exports = function (${2:args}) {
  ${0}
}
```

- **[fn]** named function
```js
function ${1:name} (${2:args}) {
  ${0}
}
```

- **[afn]** anonymous function
```js
function (${1:args}) {
  ${0}
}
```

- **[ofn]** named function as object property
```js
${1:name}: function ${1:name} (${2:args}) {
  ${0}
}
```

- **[oafn]** anonymous function as object property
```js
${1:name}: function (${2:args}) {
  ${0}
}
```

- **[fixture]** fixture function (useful when assert.throws)
```js
function fixture () {
  ${1:fnName}
}${0}
```

- **[iife]** immediately-invoked function expression
```js
;(function () {
    ${0:// body...}
})()
```


### assert

- **[ase]** assert equal
```js
assert.equal(actual, expected, msg)
```

- **[asn]** assert notEqual
```js
assert.notEqual(actual, expected, msg)
```

- **[asse]** assert strictEqual
```js
assert.strictEqual(actual, expected, msg)
```

- **[assn]** assert notStrictEqual
```js
assert.notStrictEqual(actual, expected, msg)
```

- **[asd]** assert deepEqual
```js
assert.deepEqual(actual, expected, msg)
```

- **[asdn]** assert notDeepEqual
```js
assert.notDeepEqual(actual, expected, msg)
```

- **[assd]** assert.deepStrictEqual
```js
assert.deepStrictEqual(actual, expected, msg)
```

- **[assdn]** assert.notDeepStrictEqual
```js
assert.notDeepStrictEqual(actual, expected, msg)
```

- **[asi]** assert.ifError
```js
assert.ifError(actual, expected, msg)
```

- **[ast]** assert.throws
```js
assert.throws(actual, expected, msg)
```

- **[aste]** assert.throws fixture Error
```js
assert.throws(fixture, Error)
```

- **[asttype]** assert.throws fixture TypeError
```js
assert.throws(fixture, TypeError)
```

- **[astre]** assert.throws fixture regexp message
```js
assert.throws(fixture, /expected msg/)
```

### testing

- **[desc]** describe
```js
describe('description', function () {
  // body
})
```

- **[ita]** it async
```js
it('description', function (done) {
  // body
  done()
})
```

- **[its]** it sync
```js
it('description', function (done) {
  // body
})
```

### console and misc

- **[cl]** console.log
```js
console.log(actual)
```

- **[ce]** console.error
```js
console.error(actual)
```

- **[self]** self this
```js
var self = this
```

- **[us]** use strict
```js
'use strict'
```

- **[loop]** fast while loop
```js
var len = ${1:arr}.length
var i = 0

while (i < len) {
  var val = ${1:arr}[${2:i++}]
  ${0}
}
```

- **[singleton]** singleton pattern
```js
function ${1:ClassName} (${2:options}) {
  if (!(this instanceof ${1:ClassName})) {
    return new ${1:ClassName}(${2:options});
  }
  ${0}
}
```


## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/tunnckoCore/always-callback/issues/new).  
But before doing anything, please read the [CONTRIBUTING.md](./CONTRIBUTING.md) guidelines.


## [Charlike Make Reagent](http://j.mp/1stW47C) [![new message to charlike][new-message-img]][new-message-url] [![freenode #charlike][freenode-img]][freenode-url]

[![tunnckocore.tk][author-www-img]][author-www-url] [![keybase tunnckocore][keybase-img]][keybase-url] [![tunnckoCore npm][author-npm-img]][author-npm-url] [![tunnckoCore twitter][author-twitter-img]][author-twitter-url] [![tunnckoCore github][author-github-img]][author-github-url]


[author-www-url]: http://www.tunnckocore.tk
[author-www-img]: https://img.shields.io/badge/www-tunnckocore.tk-fe7d37.svg

[keybase-url]: https://keybase.io/tunnckocore
[keybase-img]: https://img.shields.io/badge/keybase-tunnckocore-8a7967.svg

[author-npm-url]: https://www.npmjs.com/~tunnckocore
[author-npm-img]: https://img.shields.io/badge/npm-~tunnckocore-cb3837.svg

[author-twitter-url]: https://twitter.com/tunnckoCore
[author-twitter-img]: https://img.shields.io/badge/twitter-@tunnckoCore-55acee.svg

[author-github-url]: https://github.com/tunnckoCore
[author-github-img]: https://img.shields.io/badge/github-@tunnckoCore-4183c4.svg

[freenode-url]: http://webchat.freenode.net/?channels=charlike
[freenode-img]: https://img.shields.io/badge/freenode-%23charlike-5654a4.svg

[new-message-url]: https://github.com/tunnckoCore/messages
[new-message-img]: https://img.shields.io/badge/send%20me-message-green.svg
