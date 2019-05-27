### ABC031
[問題ページ](https://atcoder.jp/contests/abc031/tasks)

### A-ゲーム
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const D = parseInt(arg.split("\n")[0].split(" ")[1]);
    
    if((A+1) * D > A * (D+1)) {
        console.log((A+1) * D);
    } else {
        console.log(A * (D+1));
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-運動管理
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const min = ~~arg[0].split(" ")[0];
    const max = ~~arg[0].split(" ")[1];
    const N   = ~~arg[1];
    const A   = arg.slice(2, N + 2);
    
    for(let i in A) {
        if(A[i] < min) {
            console.log(min - A[i]);
        } else if(A[i] <= max) {
            console.log(0);
        } else {
            console.log(-1);
        }
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```