### ABC129
[問題ページ](https://atcoder.jp/contests/abc129/tasks)

### A-Airplane
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const distances = arg[0].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    console.log(distances[0] + distances[1]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Balance
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const weights = arg[1].split(" ").map(n=>parseInt(n));
    
    let   right  = weights.reduce((m,n)=>m+n);
    let   left   = 0;
    let   answer = right;
    
    for(let i in weights) {
        left  += weights[i];
        right -= weights[i];
        answer = Math.min(answer, Math.abs(left - right));
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Typical Stairs
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const dangers = arg.slice(1, M + 1);
    
    let answer = [...Array(N + 1)].fill(1);
    let broken = -1;
    let NG     = false;
    
    for(let i in dangers) {
        if(broken + 1 === dangers[i]) {
            NG = true;
        }
        
        answer[dangers[i]] = 0;
        broken = dangers[i];
    }
    
    for(let i=2; i<=N; i++) {
        answer[i] = answer[i] * (answer[i - 2] + answer[i - 1]) % 1000000007;
    }
    
    console.log(answer[N]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```