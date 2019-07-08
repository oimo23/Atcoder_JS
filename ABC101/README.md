### ABC101
[問題ページ](https://atcoder.jp/contests/abc101/tasks)

### A-Eating Symbols Easy
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    const S = N.split("").map(n=>parseInt(n)).reduce((m,n)=>m+n);
    console.log(N % S === 0 ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Digit Sums
```JavaScript
"use strict";

const main = arg => {
    const minus = arg.split("\n")[0].split("").filter(n=>n=="-").length;
    const plus  = 4 - minus;
    console.log(plus - minus);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```