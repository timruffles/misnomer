# cjs-rename

## This module doesn't exist - should it? Is there another out there already?

Given a module a bad name? Used all over your codebase and tests? Sounds like you want to rename a CJS module, and this here module can do that for you:

```sh
$ rename-module /src/some-bad-name.js some-good-name.js src/**/*.js test/**/*.js
Renaming:
- moved src/some-bad-name.js to /src/some-good-name.js
- src/foo/bar.js fixed 2 require()s
- src/foo/qux.js fixed 3 require()s
- test/foo/bar.js fixed 1 require()
- moved test/unit/some-bad-name-test.js to test/unit/some-good-name.js
```

and magically, where you saw:

```javascript
// test/unit/some-bad-name.js
require("../../src/some-bad-name.js");
```

you'll now find

```javascript
// test/unit/some-good-name.js
require("../../src/some-good-name.js");
```

Woohoo!

