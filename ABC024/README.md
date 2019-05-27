### ABC024
[問題ページ](https://atcoder.jp/contests/abc024/tasks)

### A-動物園
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = ~~arg[0].split(" ")[0];
    const B = ~~arg[0].split(" ")[1];
    const C = ~~arg[0].split(" ")[2];
    const K = ~~arg[0].split(" ")[3];
    const S = ~~arg[1].split(" ")[0];
    const T = ~~arg[1].split(" ")[1];
    
    let fee = (A * S) + (B * T);
    let discount = 0;
    
    if(S + T >= K) {
        discount = C * (S + T);   
    }
    
    console.log(fee - discount);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-自動ドア
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const T = ~~arg[0].split(" ")[1];
    const times = arg.slice(1, N + 1).map(n=>~~n);
    
    let answer = 0;
    
    for(let i in times) {
        let diffToNext = times[~~i + 1] - times[i];
        
        if(diffToNext < T) {
            answer += diffToNext;
        } else {
            answer += T;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```