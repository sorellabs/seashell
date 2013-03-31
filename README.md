# Seashell [![Build Status](https://travis-ci.org/killdream/seashell.png)](https://travis-ci.org/killdream/seashell) ![Dependencies Status](https://david-dm.org/killdream/seashell.png)

A beautiful way of running child_processes. I promise you!


### Example

```js
var seashell = require('seashell')

var ps = seashell('ps', {})
var grep = seashell('grep', {})

grep(ps('ax'), 'ssh').then(function(data) {
  console.log(data.stdout)
}, function(data) {
  console.log(data.stderr)
})
```


### Installing

Just grab it from NPM:

    $ npm install seashell


### Documentation

A quick reference of the API can be built using [Calliope][]:

    $ npm install -g calliope
    $ calliope build


### Tests

You can run all tests using Mocha:

    $ npm test


### Licence

MIT/X11. ie.: do whatever you want.

[Calliope]: https://github.com/killdream/calliope
[es5-shim]: https://github.com/kriskowal/es5-shim
