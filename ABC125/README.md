### ABC125
[問題ページ](https://atcoder.jp/contests/abc125/tasks)

### A-Biscuit Generator
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const A = ~~arg[0].split(" ")[0];
    const B = ~~arg[0].split(" ")[1];
    const T = ~~arg[0].split(" ")[2];
    
    console.log(B * Math.floor(T / A));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Resale
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const V = arg[1].split(" ").map(n=>~~n);
    const C = arg[2].split(" ").map(n=>~~n);
    
    let answer = 0;
    
    for(let i=0; i<N; i++) {
        if(V[i] - C[i] < 0) {
            
        } else {
            answer += V[i] - C[i];
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### D-Flipping Signs
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const b = arg[1].split(" ").map(n=>~~n);
    
    const minusCnt = b.filter(n=>n<0).length;
    
    
    if(minusCnt % 2 === 0) {
        console.log(b.map(n=>Math.abs(n)).reduce((m,n)=>m+n));
    } else {
        console.log(b.map(n=>Math.abs(n)).reduce((m,n)=>m+n) - (b.map(n=>Math.abs(n)).sort((a,b)=>a-b)[0] * 2));
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```