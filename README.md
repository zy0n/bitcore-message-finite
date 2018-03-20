# Finite Message Verification and Signing for Bitcore-Finite


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-finite.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-finite)
[![Build Status](https://img.shields.io/travis/zy0n/bitcore-message-finite.svg?branch=master&style=flat-square)](https://travis-ci.org/zy0n/bitcore-message-finite)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-finite.svg?style=flat-square)](https://coveralls.io/r/zy0n/bitcore-message-finite?branch=master)

bitcore-message-finite adds support for verifying and signing finite messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-finite repo](https://github.com/zy0n/bitcore-finite) for more information.

## Getting Started

```sh
npm install bitcore-message-finite
```

```sh
bower install bitcore-message-finite
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-finite');
var Message = require('bitcore-message-finite');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/zy0n/bitcore-finite/blob/master/CONTRIBUTING.md) on the main bitcore-finite repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

