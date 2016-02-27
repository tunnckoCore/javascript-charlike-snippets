## javascript-charlike-snippets

> My SublimeText 2/3 snippets. From BDD through `assert` to singleton pattern, es6 fat arrows and es6 import


## Rebuilding
```
zip javascript-charlike-snippets.sublime-package -r javascript-charlike-snippets && cp javascript-charlike-snippets.sublime-package ~/.config/sublime-text-3/Installed\ Packages/
```


## Code Style

[![standard][standard-image]][standard-url]

This snippets use [`standard`][standard-url] to maintain code style and consistency, and to avoid style arguments. You are encouraged to install it globally.

[standard-image]: https://cdn.rawgit.com/feross/standard/master/badge.svg
[standard-url]: https://github.com/feross/standard


## Table of Contents
- [module system](#module-system)
  + `rr` node variable require
  + `req` node require
  + `imp` javascript import
- [functions-and-arrows](#functions-and-arrows)
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
- [assert](#assert)
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
- [testing](#testing)
  + `desc` describe
  + `ita` it async
  + `its` it sync
- [console and misc](#console-and-misc)
  + `cl` console.log
  + `ce` console.error
  + `self` self this
  + `us` use strict
  + `loop` fast while loop
  + `singleton` singleton pattern
  + `var` variable assigning, e.g. `var foo = bar`
  + `iftypeof` if block with typeof check
  + `iferr` if block with typeof check and throw TypeError
  + `typeof` typeof check with strict equality


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

### assert

- **[ase]** assert equal

```js
${1:assert}.equal(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[asn]** assert notEqual

```js
${1:assert}.notEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[asse]** assert strictEqual

```js
${1:assert}.strictEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[assn]** assert notStrictEqual

```js
${1:assert}.notStrictEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[asd]** assert deepEqual

```js
${1:assert}.deepEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[asdn]** assert notDeepEqual

```js
${1:assert}.notDeepEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[assd]** assert.deepStrictEqual

```js
${1:assert}.deepStrictEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[assdn]** assert.notDeepStrictEqual

```js
${1:assert}.notDeepStrictEqual(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[asi]** assert.ifError

```js
${1:assert}.ifError(${2:err})${0}
```

- **[ast]** assert.throws

```js
${1:assert}.throws(${2:actual}, ${3:expected}, ${4:msg})${0}
```

- **[aste]** assert.throws fixture Error

```js
${1:assert}.throws(${2:fixture}, Error)${0}
```

- **[asttype]** assert.throws fixture TypeError

```js
${1:assert}.throws(${2:fixture}, TypeError)${0}
```

- **[astre]** assert.throws fixture regexp message

```js
${1:assert}.throws(${2:fixture}, /${3:expected msg}/)${0}
```

### testing

- **[desc]** describe

```js
${1:describe}('${2:description}', function () {
  ${0}
})
```

- **[ita]** it async

```js
${1:it}('${2:description}', function (${3:done}) {
  ${0}
  ${4:done}()
})
```

- **[its]** it sync

```js
${1:it}('${2:description}', function () {
  ${0}
})
```

### console and misc

- **[cl]** console.log

```js
console.log(${1:actual})${0}
```

- **[ce]** console.error

```js
console.error(${1:actual})${0}
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
    return new ${1:ClassName}(${2:options})
  }
  ${0}
}
```

- **var** variable assigning

```js
var ${2:foo} = ${1:bar}${0}
```

- **[iftypeof]** if block with typeof check

```js
if (typeof ${1:actual} === ${2:expected}) {
  ${0}
}
```

- **[iferr]** if block with typeof check and throw TypeError

```js
if (typeof ${1:actual} === ${2:expected}) {
  throw new ${3:TypeError}('${4:message}')
}${0}
```


- **[typeof]** typeof check with strict equality

```js
typeof ${1:actual} === ${2:expected}
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
