### ABC086
[問題ページ](https://atcoder.jp/contests/abc086/tasks)

### A-Product
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    console.log((A * B) % 2 === 0 ? "Even" : "Odd");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-1 21
```JavaScript
"use strict";
    
const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    
    const N = parseInt(A + B);
    for(let i=1; i<N; i++) {
        if(Math.pow(i, 2) === N) {
            console.log("Yes");
            return;
        } 
    }
    
    console.log("No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Traveling
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const plan = arg.slice(1, N + 1);
    
    let x  = 0;
    let y  = 0;
    let lt = 0;
    
    for(let i in plan) {
        let t  = parseInt(plan[i].split(" ")[0]);
        let dx = parseInt(plan[i].split(" ")[1]);
        let dy = parseInt(plan[i].split(" ")[2]);
        
        let distance = Math.abs(dx - x) + Math.abs(dy - y);
        
        if(distance > t - lt || distance % 2 !== (t - lt) % 2) {
            console.log("No");
            return;
        }
        
        x  = dx;
        y  = dy;
        lt = t;
    }
    
    console.log("Yes");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```