# hthcoin Message Verification and Signing for hthcore

hthcore-message adds support for verifying and signing hthcoin messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore repo](https://github.com/bitpay/bitcore) for more information.

## Getting Started

```sh
npm install hthcore-message
```

```sh
bower install hthcore-message
```

To sign a message:

```javascript
var hthcore = require('hthcore-lib');
var Message = require('hthcore-message');

var privateKey = hthcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.
Copyright 2018 hthcoin Core Developers
