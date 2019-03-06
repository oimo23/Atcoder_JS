### ABC102
[問題ページ](https://atcoder.jp/contests/abc102/tasks)

### A-Multiple of 2 and N
```JavaScript
'use strict';

function main(arg) {
    const N = arg.split("\n")[0];
    console.log( N % 2 === 0 ? N : N * 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Maximum Difference
```JavaScript
"use strict";

function main(arg) {
    const A = arg.split("\n")[1].split(" ").sort((a,b)=>a-b);
    console.log(A[A.length-1] - A[0]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```