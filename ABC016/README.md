### ABC016
[問題ページ](https://atcoder.jp/contests/abc016/tasks)

### A-12月6日
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n")[0].split(" ");
    const M = parseInt(arg[0]);
    const D = parseInt(arg[1]);
    
    console.log(M % D === 0 ? "YES" : "NO");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-A±B Problem
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n")[0].split(" ");
    const A = ~~arg[0];
    const B = ~~arg[1];
    const C = ~~arg[2];
    
    if(A + B === C && A - B === C) {
        console.log("?");
    } else if(A + B === C) {
        console.log("+");
    } else if(A - B === C) {
        console.log("-");
    } else {
        console.log("!");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```