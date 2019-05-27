### ABC127
[問題ページ](https://atcoder.jp/contests/abc127/tasks)

### A-Ferris Wheel
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const A = parseInt(arg[0].split(" ")[0]);
    const B = parseInt(arg[0].split(" ")[1]);
    
    if(A >= 13) {
        console.log(B);
    } else if(13 > A && A >= 6) {
        console.log(B / 2);
    } else {
        console.log(0);
    }
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Algae
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const r = parseInt(arg[0].split(" ")[0]);
    const D = parseInt(arg[0].split(" ")[1]);
    let X = parseInt(arg[0].split(" ")[2]);
    
    for(let i=0; i<10; i++) {
        let temp = (r * X) - D;
        console.log(temp);
        
        X = temp;
    }
    
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Prison
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const M = parseInt(arg[0].split(" ")[1]);
    
    const LR = arg.slice(1, M + 1);
    let low  = parseInt(LR[0].split(" ")[0]);
    let high = parseInt(LR[0].split(" ")[1]);
    
    for(let i in LR) {
        let L = parseInt(LR[i].split(" ")[0]);
        let R = parseInt(LR[i].split(" ")[1]);
        
        if(high < L) {
            console.log(0);
            return;
        }
        
        if(low > R) {
            console.log(0);
            return;
        }
        
        if(low < L) {
            low = L;
        }
        
        if(high > R) {
            high = R;
        }
    }

    
    console.log((high - low) + 1);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```