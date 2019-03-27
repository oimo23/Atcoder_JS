### ABC083
[問題ページ](https://atcoder.jp/contests/abc083/tasks)

### A-Libra
```JavaScript
"use strict";

function main(arg) {
    const W = arg.split("\n")[0].split(" ").map(n=>parseInt(n));
    const L = W[0] + W[1];
    const R = W[2] + W[3];
    
    if(L > R) {
        console.log("Left");
    } else if ( L < R) {
        console.log("Right");
    } else {
        console.log("Balanced");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Some Sums
```JavaScript
"use strict";
    
const main = arg => {
    const N  = arg.split("\n")[0].split(" ")[0];
    const A  = arg.split("\n")[0].split(" ")[1];
    const B  = arg.split("\n")[0].split(" ")[2];
    let list = [];
    
    for(let i=1; i<=N; i++) {
        let sum = parseInt(String(i).split("").reduce((m,n)=>parseInt(m)+parseInt(n)));
        if(sum >= A && sum <= B) list.push(i);
    }
    
    console.log(list.reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```