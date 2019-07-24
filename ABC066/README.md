### ABC066
[問題ページ](https://atcoder.jp/contests/abc066/tasks)

### A-ringring
```JavaScript
"use strict";

const main = arg => {
    const prices = arg.split("\n")[0].split(" ").map(n=>parseInt(n));

    console.log(prices.sort((a,b)=>a-b).slice(0,2).reduce((m,n)=>m+n));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-pushpush
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = ~~arg[0];
    const b = arg[1].split(" ").map(n=>~~n);
    
    let answer = [];
    
    if(N % 2 === 0) {
        for(let i=N-1; i>0; i -= 2) {
            answer.push(b[i]);
        }
        
        for(let i=0; i<N; i += 2) {
            answer.push(b[i]);
        }
    } else {
        for(let i=N-1; i>=0; i -= 2) {
            answer.push(b[i]);
        }
        
        for(let i=1; i<N; i += 2) {
            answer.push(b[i]);
        }
    }
    
    console.log(answer.join(" "));
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```