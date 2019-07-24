### ABC063
[問題ページ](https://atcoder.jp/contests/abc063/tasks)

### A-Restricted
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0].split(" ").map(n=>parseInt(n)).reduce((m,n)=>m+n);
    console.log(N < 10 ? N : "error" );
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Varied
```JavaScript
"use strict";

const main = arg => {
    const S   = arg.split("\n")[0].split("");
    const set = new Set(S);
    
    console.log(S.length == set.size ? "yes" : "no");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Bugged
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const scores = arg.slice(1, N + 1).map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    let myScore = scores.reduce((m,n)=>m+n);
    
    if(myScore % 10 === 0) {
        for(let i in scores) {
            if((myScore - scores[i]) % 10 !== 0) {
                console.log(myScore - scores[i]);
                return;
            }
        }
    } else {
        console.log(myScore);
        return;
    }
    
    console.log(0);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```