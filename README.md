# bip21-max
[![Version](http://img.shields.io/npm/v/bip21-max.svg)](https://www.npmjs.org/package/bip21-max)

A [BIP21](https://github.com/bitcoin/bips/blob/master/bip-0021.mediawiki) compatible URL encoding library.


## Example

``` javascript
var bip21 = require('bip21-max')

var decoded = bip21.decode('maxcoin:mNpmPa1UAh8VdK8nDy8GAhHrefmmrMJfmF?amount=20.3&label=Foobar')

console.log(decoded)
// { address: 'mNpmPa1UAh8VdK8nDy8GAhHrefmmrMJfmF',
//   options: {
//     amount: 20.3,
//     label: 'Foobar' }
// }
//
// WARNING: Remember to error check the `.address`!

console.log(bip21.encode('mNpmPa1UAh8VdK8nDy8GAhHrefmmrMJfmF'))
// => smartcash:Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5

console.log(bip21.encode('mNpmPa1UAh8VdK8nDy8GAhHrefmmrMJfmF', {
	amount: 20.3,
	label: 'Foobar'
}))
// => smartcash:Sfra8YaJ5UL7R6ZMg3ZH2pZLcDQP71vFQ5?amount=20.3&label=Foobar
```


## License [MIT](LICENSE)
