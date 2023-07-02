Repro with:

```
$ bun install
$ bun run index.mts
[0.07ms] ".env.development", ".env"
1 | 'use strict'
2 |
3 | // like String.prototype.search but returns the last index
4 | function _searchLast (str, rgx) {
5 |   const matches = Array.from(str.matchAll(rgx))
                                ^
TypeError: undefined is not an object (evaluating 'str.matchAll')
      at _searchLast (/Users/dan/Projects/bun-typeerror-2023-07-02/node_modules/dotenv-expand/lib/main.js:5:29)
      at _interpolate (/Users/dan/Projects/bun-typeerror-2023-07-02/node_modules/dotenv-expand/lib/main.js:12:39)
      at expand (/Users/dan/Projects/bun-typeerror-2023-07-02/node_modules/dotenv-expand/lib/main.js:68:6)
      at /Users/dan/Projects/bun-typeerror-2023-07-02/index.mts:5:0
      at globalThis (/Users/dan/Projects/bun-typeerror-2023-07-02/index.mts:7:23)
```
