### ABC132
[問題ページ](https://atcoder.jp/contests/abc132/tasks)

### A-Fifty-Fifty
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const S = arg[0].split("");
    const set = new Set(S);
    const unique = [...set];
    
    if(set.size !== 2) {
        console.log("No");
        return;
    }
    
    for(let i in unique) {
        if(S.filter(n=>n===unique[i]).length !== 2) {
            console.log("No");
            return;
        }
    }
    
    console.log("Yes");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### B-Ordinary Number
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const p = arg[1].split(" ").map(n=>parseInt(n));
    
    let answer = 0;
    
    for(let i=0; i<N-2; i++) {
        let left   = p[i];
        let middle = p[parseInt(i) + 1];
        let right  = p[parseInt(i) + 2];
        
        let array = [left, middle, right].sort((a,b)=>a-b);
        
        if(array[1] === middle) {
            answer++;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Divide the Problems
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0]);
    const d = arg[1].split(" ").map(n=>parseInt(n)).sort((a,b)=>a-b);
    
    const middleHigh = d[N / 2];
    const middleLow  = d[(N / 2) - 1];
    
    console.log(middleHigh - middleLow);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```