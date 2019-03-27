### ABC074
[問題ページ](https://atcoder.jp/contests/abc074/tasks)

### A-Bichrome Cells
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0];
    const B = arg.split("\n")[1];
    console.log((A * A) - B);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```