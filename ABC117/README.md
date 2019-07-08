### ABC117
[問題ページ](https://atcoder.jp/contests/abc117/tasks)

### A-Entrance Examination
```JavaScript
const main = arg => {
    console.log(arg.split(" ")[0] / arg.split(" ")[1]);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Polygon
```JavaScript
'use strict';

const main = arg => {
    const N = arg.split("\n")[0];
    const L = arg.split("\n")[1].split(" ").map(n=>parseInt(n));
    
    const max    = Math.max(...L);
    const others = L.reduce((m,n)=>m+n) - max;
    
    console.log(max < others ? 'Yes' : 'No');
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Streamline
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0].split(" ")[0];
    const M = ~~arg[0].split(" ")[1];
    const X = arg[1].split(" ").map(n=>~~n).sort((a,b)=>a-b);
    
    // ソートして、差の大きい順で分ける
    let diffs = [];
    
    for(let i in X) {
        if(X[~~i+1] - X[i]) {
            diffs.push(X[~~i+1] - X[i]);
        }
    }
    
    if(!diffs.length || N >= M) {
        console.log(0);
        return;
    }
    
    diffs.sort((a,b)=>b-a);
    let answer = diffs.reduce((m,n)=>m+n);

    for(let i=0; i<N-1; i++) {
        answer -= diffs[i];
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```