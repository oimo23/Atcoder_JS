### ABC037
[問題ページ](https://atcoder.jp/contests/abc037/tasks)

### A-饅頭
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    const C = arg.split("\n")[0].split(" ")[2];
    
    console.log(Math.floor(C / Math.min(A, B)));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-編集
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const Q = ~~arg[0].split(" ")[1];
    
    const a = [...Array(N)].fill(0);
    const steps = arg.slice(1, Q + 1).map(n=>n.split(" ").map(m=>~~m));
    
    for(let i=0; i<steps.length; i++) {
        const l = steps[i][0];
        const r = steps[i][1];
        const t = steps[i][2];
        
        for(let j=l - 1; j<r; j++) {
            a[j] = t;
        }
    }
    
    console.log(a.join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```