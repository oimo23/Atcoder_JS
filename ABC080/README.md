### ABC080
[問題ページ](https://atcoder.jp/contests/abc080/tasks)

### A-Parking
```JavaScript
"use strict";

function main(arg) {
    arg = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const N = arg[0];
    const A = arg[1];
    const B = arg[2];
    
    console.log(A * N < B ? A * N : B);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Harshad Number
```JavaScript
"use strict";
    
const main = arg => {
    const N   = arg.split("\n")[0];
    const sum = N.split("").map(n=>parseInt(n)).reduce((m,n)=>m+n);
    console.log(N % sum == 0 ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```