### ABC057
[問題ページ](https://atcoder.jp/contests/abc057/tasks)

### A-Remaining Time
```JavaScript
"use strict";
    
const main = arg => {
    arg     = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const A = arg[0];
    const B = arg[1];
    
    console.log(A + B >= 24 ? (A + B) - 24 : A + B);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```