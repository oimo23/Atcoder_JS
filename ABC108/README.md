### ABC108
[問題ページ](https://atcoder.jp/contests/abc108/tasks)

### A-Pair
```JavaScript
"use strict";

const main = arg => {
    arg = parseInt(arg);
    const evenCnt = Math.floor(arg / 2);
    const oddCnt  = arg - evenCnt;
    console.log(evenCnt * oddCnt);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```