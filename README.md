# express-catch-errors

Generated by [OSS Project Generator](http://bit.ly/generator-oss-project).

[![NPM Version][npm-badge]][npm-url]
[![License][license-badge]][license-url]

> A high-order function to catch errors from promises.

# Installation

Install package

```bash
$ npm install --save express-catch-errors
```

# Usage

* Router

```js
// user.router.js
const userController = require('./user.controller');

router.get('/users', catchErrors(userController.list));
```

* Controller

```js
// user.controller.js
const mongoose = require('mongoose');
const User = mongoose.model('User');

module.exports.list = async (req, res) => {
  const users = await User.find();

  res.json(users);
};
```

# Development

* Cloning the repo

```bash
$ git clone https://github.com/robertoachar/express-catch-errors.git
```

* Installing dependencies

```bash
$ npm install
```

* Running scripts

Action | Usage
---    | ---
Starting development mode | `npm start`
Linting code              | `npm run lint`

# Author

[Roberto Achar](https://twitter.com/robertoachar)

# License

[MIT](https://github.com/robertoachar/express-catch-errors/blob/master/LICENSE)

[npm-badge]: https://img.shields.io/npm/v/express-catch-errors.svg
[npm-url]: https://www.npmjs.com/package/express-catch-errors

[license-badge]: https://img.shields.io/github/license/robertoachar/express-catch-errors.svg
[license-url]: https://opensource.org/licenses/MIT
