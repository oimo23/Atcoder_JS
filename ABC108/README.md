### ABC108
[問題ページ](https://atcoder.jp/contests/abc108/tasks)

### A-Pair
```JavaScript
'use strict';

function main(arg) {
    arg = parseInt(arg);
    let evenCnt = Math.floor(arg / 2);
    let oddCnt  = arg - evenCnt;
    console.log(evenCnt * oddCnt);
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```