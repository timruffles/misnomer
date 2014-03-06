# cjs-rename

Given a module a bad name? Used all over your codebase and tests? Sounds like you want to rename a CJS module, and this here module can do that for you:

```sh
$ rename-module /src/some-bad-name.js some-good-name.js src/**/*.js test/**/*.js
Renaming:
- src/foo/bar.js 2 occurrences
- src/foo/qux.js 1 occurrence
- test/foo/bar.js 1 occurrence
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

