### ABC106
[問題ページ](https://atcoder.jp/contests/abc106/tasks)

### A-Garden
```JavaScript
'use strict'

function main(arg) {
    let A = parseInt(arg.split(" ")[0]);
    let B = parseInt(arg.split(" ")[1]);
    console.log((A * B) - (A + B - 1));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-105
```JavaScript
"use strict";

function main(arg) {
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