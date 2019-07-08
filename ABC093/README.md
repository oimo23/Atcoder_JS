### ABC093
[問題ページ](https://atcoder.jp/contests/abc093/tasks)

### A-abc of ABC
```JavaScript
"use strict";

const main = arg => {
    const S = arg.split("\n")[0].split("");
    if(S.some(n=>n=="a") && S.some(n=>n=="b") && S.some(n=>n=="c")) {
        console.log("Yes");
    } else {
        console.log("No");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Small and Large Integers
```JavaScript
"use strict";
    
const main = arg => {
    arg     = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const A = arg[0];
    const B = arg[1];
    const K = arg[2];
    
    let N = [];
    
    for(let i=0; i<K; i++) {
        if((A+i) > B) break;
        N.push(A+i);
    }
    
    for(let i=0; i<K; i++) {
        if((B-i) < A) break;
        N.push(B-i);
    }
    
    let set = new Set(N);
    
    console.log([...set].sort((a,b)=>a-b).join("\n"));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```