### ABC044
[問題ページ](https://atcoder.jp/contests/abc044/tasks)

### A-高橋君とホテルイージー
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    const K = arg.split("\n")[1];
    const X = arg.split("\n")[2];
    const Y = arg.split("\n")[3];
    
    console.log(N - K > 0 ? (X * K) + Y * (N - K) : X * N);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```