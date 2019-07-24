### ABC048
[問題ページ](https://atcoder.jp/contests/abc048/tasks)

### A-AtCoder *** Contest
```JavaScript
"use strict";
    
const main = arg => {
    const s = arg.split("\n")[0].split(" ")[1].split("")[0];
    
    console.log("A" + s + "C");
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```

### C-Boxes and Candies
```JavaScript
"use strict";
    
const main = arg => {
    arg = arg.trim().split("\n");
    const N = parseInt(arg[0].split(" ")[0]);
    const X = parseInt(arg[0].split(" ")[1]);
    
    const A = arg[1].split(" ").map(n=>parseInt(n));
    
    let answer = 0;
    
    for(let i in A) {
        if(A[i] > X) {
            answer += A[i] - X;
            A[i] = X;
        }
    }

    for(let i=0; i<A.length-1; i++) {
        let temp = A[i] + A[parseInt(i) + 1];
        
        if(temp > X) {
            answer += temp - X;
            A[parseInt(i) + 1] -= temp - X;
        }
    }
    
    console.log(answer);
}
main(require('fs').readFileSync('/dev/stdin', 'utf8'));

```