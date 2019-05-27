### ABC030
[問題ページ](https://atcoder.jp/contests/abc030/tasks)

### A-勝率計算
```JavaScript
"use strict";

const main = arg => {
    const A = parseInt(arg.split("\n")[0].split(" ")[0]);
    const B = parseInt(arg.split("\n")[0].split(" ")[1]);
    const C = parseInt(arg.split("\n")[0].split(" ")[2]);
    const D = parseInt(arg.split("\n")[0].split(" ")[3]);
    
    if((B / A) === (D / C) ) {
        console.log("DRAW");
        return;
    }
    
    console.log((B / A) > (D / C) ? "TAKAHASHI" : "AOKI")
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-時計盤
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0] % 12;
    const M = ~~arg[0].split(" ")[1];
    
    const longDegree  = N * 30 + M * 0.5;
    const shortDegree = M * 6;
    
    const abs = Math.abs(longDegree - shortDegree);
    
    console.log(abs <= 180 ? abs : 360 - abs);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```