### ABC116
[問題ページ](https://atcoder.jp/contests/abc116/tasks)

### A-Right Triangle
```JavaScript
"use strict"

const main = arg => {
    const temp = arg.split(" ");
    console.log((temp[0] * temp[1]) / 2);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Collatz Problem
```JavaScript
"use strict";

const main = arg => {
    let s = parseInt(arg);
    let memo  = new Set();
    let cnt = 1;
    
    memo.add(s);
    
    while(true) {
        cnt++;
        if(s % 2 === 0) {
            s = s / 2;
            if(memo.has(s)) {
                console.log(cnt);
                break;
            }
            memo.add(s);
        } else {
            s = (s * 3) + 1;
            if(memo.has(s)) {
                console.log(cnt);
                break;
            }
            memo.add(s);
        }
    }
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Monsters Battle Royale
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const h = arg[1].split(" ").map(n=>parseInt(n));
    
    const state = [...Array(N)].fill(0);
    let answer  = 0;
    let action  = 0;
    
    for(let i=0; i<N; i++) {
        if(action >= h[i]) {
            action = h[i];
        } else {
            answer += h[i] - action;
            action = h[i];
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```