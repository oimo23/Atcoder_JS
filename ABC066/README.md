### ABC066
[問題ページ](https://atcoder.jp/contests/abc066/tasks)

### A-ringring
```JavaScript
"use strict";

const main = arg => {
    const prices = arg.split("\n")[0].split(" ").map(n=>parseInt(n));

    console.log(prices.sort((a,b)=>a-b).slice(0,2).reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```