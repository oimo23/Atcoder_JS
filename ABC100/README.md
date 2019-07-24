### ABC100
[問題ページ](https://atcoder.jp/contests/abc100/tasks)

### A-Happy Birthday!
```JavaScript
"use strict";

const main = arg => {
    const A = arg.split("\n")[0].split(" ")[0];
    const B = arg.split("\n")[0].split(" ")[1];
    if(A <=8 && B <=8) {
        console.log("Yay!");
    } else {
        console.log(":(");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Ringo's Favorite Numbers
```JavaScript
"use strict";
 
const main = arg => {
    arg = arg.split("\n")[0].split(" ");
    const D = arg[0];
    const N = arg[1] == "100" ? "101" : arg[1];
    let zeros = [];
    
    if(parseInt(N) === 0) {
        console.log(0);
        return;
    }
    
    for(let i=0; i<D; i++) {
        zeros.push("00");
    }
    
    console.log(N + zeros.join(""));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-*3 or /2
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const a = arg[1].split(" ").map(n=>~~n);
    
    const limit = [];
    
    for(let i in a) {
        let cnt = 0;
        
        while(a[i] % 2 === 0 || a[i] === 0) {
            a[i] = a[i] / 2;
            cnt++;
        }
        
        limit.push(cnt);
        cnt = 0;
    }
    
    console.log(limit.reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```