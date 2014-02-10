# strip-comments [![NPM version](https://badge.fury.io/js/strip-comments.png)](http://badge.fury.io/js/strip-comments)

> Strip block comments or line comments from code

Should work with any language that uses the same syntax, e.g. JavaScript, LESS, SASS/SCSS, CSS.

## Install

### [npm](npmjs.org)

```bash
 npm i strip-comments --save
 ```

### [bower](https://github.com/bower/bower)

```bash
 npm install strip-comments --save
 ```

## Usage

```js
var strip = require('strip-comments');
```

### all comments

```js
strip( str );
```
Removes

```js
// This comment
```
and

```js
/**
 * this
 * comment
 */
var foo = function(/* and these */) {}
```

### line comments

```js
strip.line( str );
```
Removes

```js
// This comment
```
Not

```js
/**
 * this
 * comment
 */
var foo = function(/* and these */) {}
```

### block comments

```js
strip.block( str );
```
Removes

```js
/**
 * this
 * comment
 */
var foo = function(/* and these */) {}
```
Not

```js
// This comment
```

## Tests

```bash
mocha -R spec
```


## Author

**Jon Schlinkert**

+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License
Copyright (c) 2014 Jon Schlinkert, contributors.
Released under the MIT license