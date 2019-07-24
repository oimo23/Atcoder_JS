### ABC106
[問題ページ](https://atcoder.jp/contests/abc106/tasks)

### A-Garden
```JavaScript
"use strict"

const main = arg => {
    const A = parseInt(arg.split(" ")[0]);
    const B = parseInt(arg.split(" ")[1]);
    console.log((A * B) - (A + B - 1));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-105
```JavaScript
"use strict";

const main = arg => {
    const N = parseInt(arg.split("\n")[0]);
    let answer = 0;
    
    for(let i=1; i<=N; i=i+2) {
        let cnt = 0;
        for(let j=1; j<=i; j++) {
            if(i % j === 0) {
                cnt++;
            }
        }
        if(cnt === 8) {
            answer++;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-To Infinity
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("").map(n=>parseInt(n));
    const K = parseInt(arg[1]);
    
    for(let i=0; i<K; i++) {
        if(S[i] !== 1) {
            console.log(S[i]);
            return;
        }
    }
    
    console.log(1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```