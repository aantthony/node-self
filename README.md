node-self
=========

require() relative to the path of your module.

### Installation

```bash
npm install --save --from-git git://github.com/aantthony/node-self.git
```

### Usage:

```js
var User = require('self')('lib/models/user');
```

### How does it work?

The first time node-self is called, it detects which file is calling it. It then traverses up the directory tree to find the first `package.json`. Then all calls to `node-self` will simply call `require()` relative to that directory.
