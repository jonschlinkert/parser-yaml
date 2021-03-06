# parser-yaml [![NPM version](https://badge.fury.io/js/parser-yaml.svg)](http://badge.fury.io/js/parser-yaml)

> parser-cache compatible YAML parser, using js-yaml.

## Install

### Install with [npm](npmjs.org)

```bash
npm i parser-yaml --save
```

## Run tests

```bash
npm test
```

## Usage
```js
var parser = require('parser-yaml');
```

### parse

```js
parser.parse(str, options, function(err, res) {
  if (err) { throw err; }
  console.log(res);
});
```

### parseFile

```js
parser.parseFile('fixtures/a.yml', function (err, res) {
  if (err) { throw err; }
  console.log(res);
});
```

### parseSync

```js
var res = parser.parseSync(str, options);
console.log(res);
```

## API

### [parse](index.js#L32)

* `str` **{String|Object}**: The object or string to parse.    
* `options` **{Object|Function}**: or `cb` callback function.    
* `cb` **{Function}**: callback function.    

Parse the given `str` of YAML and callback `cb(err, obj)`.

### [parseSync](index.js#L56)

* `str` **{String|Object}**: The object or string to parse.    
* `returns`: {Object}  

Parse the given `str` of YAML.

### [parseFile](index.js#L80)

YAML file support. Parse a file at the given `filepath` and callback `callback(err, obj)`.

* `filepath` **{String}**    
* `options` **{Object|Function}**: or callback function.    
* `callback` **{Function}**    

```js
parser.parseFile('foo/bar/baz.yml');
```

### [parseFileSync](index.js#L109)

YAML file support. Parse a file at the given `filepath`.

* `filepath` **{String}**    
* `options` **{Object}**: Options to pass to [js-yaml]    

```js
parser.parseFile('foo/bar/baz.yml');
```


## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/parser-yaml/issues)

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on November 24, 2014._

[parser-cache]: https://github.com/jonschlinkert/parser-cache