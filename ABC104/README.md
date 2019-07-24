### ABC104
[問題ページ](https://atcoder.jp/contests/abc104/tasks)

### A-Rated for Me
```JavaScript
"use strict";

const main = arg => {
    arg = parseInt(arg);
    
    if(arg < 1200){
        console.log("ABC");
    } else if(arg < 2800) {
        console.log("ARC");
    } else {
        console.log("AGC");
    }
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-AcCepted
```JavaScript
"use strict";

const main = arg => {
    arg = arg.split("\n");
    arg = arg[0];
    
    const indexA = arg.indexOf("A");
    const indexC = arg.indexOf("C");
    
    if(arg.split("").filter(n=>isLowerCase(n)).length !== arg.length - 2 ) {
        console.log("WA");
        return;
    }
    
    if(indexA === 0 && indexC >= 2 && indexC <= arg.length - 2) {
        console.log("AC");
    } else {
        console.log("WA");
    }
}

function isLowerCase(str){
    return str.match(/^[a-z]+$/) ? true: false;
}

main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-All Green
```JavaScript
"use strict";
    
const div = (a, b) => Math.floor(a / b);

const main = arg => {
    arg = arg.trim().split("\n");
    const D = parseInt(arg[0].split(" ")[0]);
    const G = parseInt(arg[0].split(" ")[1]);
    
    const scores = arg.slice(1, D + 1);
    
    let p = [];
    let c = [];
    
    for(let i=0; i<D; i++) {
        let temp = scores[i].split(" ").map(n=>parseInt(n));
        p[i] = temp[0];
        c[i] = temp[1];
    }
    
    let ans = 1e9;
    
    for (let mask = 0; mask < (1 << D); ++mask) {
        let s = 0, num = 0, rest_max = -1;
        
        for (let i = 0; i < D; ++i) {
            if (mask >> i & 1) {
                s += 100 * (i + 1) * p[i] + c[i];
                num += p[i];
            } else rest_max = i;
        }
        
        if (s < G) {
            let s1 = 100 * (rest_max + 1);
            let need = div(G - s + s1 - 1, s1);
            if (need >= p[rest_max]) continue;
            num += need;
        }
        
        ans = Math.min(ans, num);
    }
    
    console.log(ans);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```