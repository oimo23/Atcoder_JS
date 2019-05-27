### ABC026
[問題ページ](https://atcoder.jp/contests/abc026/tasks)

### A-掛け算の最大値
```JavaScript
"use strict";
    
const main = arg => {
    const N = arg.split("\n")[0];
    
    console.log(Math.pow((N / 2), 2));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-N重丸
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const R = arg.slice(1, N + 1).map(n=>~~n).sort((a,b)=>a-b).map(n=>Math.pow(~~n, 2));
    
    let answer = 0;
    
    for(let i in R) {
        if(i % 2 === 0) {
            answer += R[i];
        } else {
            answer -= R[i];
        }
    }
    
    console.log(Math.abs(answer * Math.PI));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```