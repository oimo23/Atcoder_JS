### ABC040
[問題ページ](https://atcoder.jp/contests/abc040/tasks)

### A-赤赤赤赤青
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ")[0];
    const X = arg.split("\n")[0].split(" ")[1];
    
    console.log(Math.min(X-1, N-X))
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-□□□□□
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    let answer = 1e5;
    
    for (let i=1; i<=Math.sqrt(N); i++) {
        const A = Math.floor(N / i);
        
        const abs = Math.abs(A - i);
        const M = N % (A * i);
        
        answer = Math.min(answer, abs + M);
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### A-柱柱柱柱柱
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const a = arg[1].split(" ");
    
    let minCost = [0, Math.abs(a[0] - a[1])];
    
    for(let i=2; i<a.length; i++) {
        const cost1 = minCost[i-2] + Math.abs(a[i] - a[i-2]);
        const cost2 = minCost[i-1] + Math.abs(a[i] - a[i-1]);
        
        minCost.push(Math.min(cost1, cost2));
    }
    
    console.log(minCost.pop());
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```