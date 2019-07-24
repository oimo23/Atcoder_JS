### ABC101
[問題ページ](https://atcoder.jp/contests/abc101/tasks)

### A-Eating Symbols Easy
```JavaScript
"use strict";

const main = arg => {
    const N = arg.split("\n")[0];
    const S = N.split("").map(n=>parseInt(n)).reduce((m,n)=>m+n);
    console.log(N % S === 0 ? "Yes" : "No");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Digit Sums
```JavaScript
"use strict";

const main = arg => {
    const minus = arg.split("\n")[0].split("").filter(n=>n=="-").length;
    const plus  = 4 - minus;
    console.log(plus - minus);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Minimization
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const K = parseInt(arg[0].split(" ")[1]);
    
    const A = arg[1].split(" ").map(n=>parseInt(n));
    
    let answer = 0;
    
    if(N <= K) {
        answer = 1;
    } else {
        answer = Math.ceil((N - K) / (K - 1)) + 1;
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```